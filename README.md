# Let's study Data Science!

Hello, my name is Jane Lee.  
This is my HOMEPAGE!   
I'm trying to share my **Knowledge** about *ROC curve*.  
Then,,, Let's join!  

## ROC curve
It's an indicator that evaluates AI that we made.  

### History
> The ROC curve was first used during World War II for the analysis of radar signals before it was employed in signal detection theory. Following the attack on Pearl Harbor in 1941, the United States army began new research to increase the prediction of correctly detected Japanese aircraft from their radar signals. -Wikipedia

### CONFUSION MATRIX  
Do you ever heard about **CONFUSION MATRIX**?  
It is the evaluation table and consist of TP, FP, TN and FN.  
Before we begin to study the confusion matrix in earnest, we need to know what "TP, FP, TN, FN" is.  
Suppose AI you made. And it predicts the result in binary(Positive or Negative).  

#### If real answer is "*POSITIVE*" about some problem.
- Our AI predicted the result to *POSITIVE*.
  - That time, We call it "True Positive(TP)".
- Our AI predicted the result to *NEGATIVE*
  - That time, We call it "False Negative(FN)".  

#### If real answer is "*NEGATIVE*" about some problem.
- Our AI predicted the result to *POSITIVE*.
  - That time, We call it "False Positive(FP)".
- Our AI predicted the result to *NEGATIVE*
  - That time, We call it "True Negative(TN)".

Then we will make CONFUSION MATRIX!  
|             |            |  Predicted |     <      |
| :---------: |  :------:  |  :------:  |  :------:  |
|             |            |  Positive  |  Negative  |
| **Real Answer** |  Positive  |     TP     |     FN     |
|     ^       |  Negative  |     FP     |     TN     |
  
*****

### Threshold
Thresholds are similar as **Base Point**.  
It divides data into "Positive" or "Negative".  
However, in my story, it would be easier to understand to think that it is a prediction of our AI.

There is a graph about some data.  
<img src = "https://user-images.githubusercontent.com/65939621/85392496-90ee4180-b586-11ea-9730-46caaeb513e6.PNG" width ="500">  

Depending on where you put threshold, Confusion Matrix's value also changes.  
(Because real result values are _already_ fixed in the graph.)  

So, there are so many Confusion matrix.  

*****

### ROC(Receiver Operating Characteristics) curve
It consists of TPR and FPR.  
According to table of Confusion Matrix, we can understand what they are.  
- TPR(True Positive Rate) = Sensitivity
  - `TP/(TP+FN)`
  - **_How many times_** did our AI choose the answer?

- FPR(False Positive Rate) = 1-Specificity
  - `FP/(FP+TN)`
  - **_How incorrectly_** did our AI choose the answer?

Set FPR to x-axis and TPR to y-axis.  
Calculate and plot the TPR and FPR of each confusion matrix.  
Then All the points become a ROC curve.  
<img src = "https://user-images.githubusercontent.com/65939621/85402051-feee3500-b595-11ea-9630-41e87642237e.png" width="400">  
In the graph, a green diagonal is the same of TPR and FPR.  
In other words, it is the probability of accidental occurrence.  
So the closer the ROC curve is to the green line, the worse our AI's ability.  
~~(Threshold = our AI's prediction)~~  
And the more similar the shape of the ROC curve to '⎾', the better our AI's ability.  

After completing ROC curve, we can decide which thresholds to use.  
Determining threshold depends on the situation in which the system is used. 

<img src = "https://user-images.githubusercontent.com/65939621/85498824-64d0d000-b61b-11ea-8579-e79e034bb572.PNG" width="500">  

*****

### Better Decision Threshold
#### Cancer Detection
Imagine a situation in which a doctor diagnoses a patient's cancer.  
(Here, understand that doctor is our AI.)  

In this situation, two wrong judgments can occur. 
```
1. The doctor diagnoses the cancer patient as normal. (=FN)  
2. The doctor diagnoses the normal patient as cancer. (=FP)   
```

'Case 1' is more **_DANGEROUS_**. The patient may miss the time to treat cancer.  
Therefore, you must determine the threshold at which FN does not occur.  
<img src = "https://user-images.githubusercontent.com/65939621/85498385-8bdad200-b61a-11ea-85a8-ea26b8e6731a.PNG" width="500">  

#### Fingerprint Doorlock
Imagine a situation where we open the door with a door lock.  
(Here, understand that Doorlook is our AI.)  

In this situation, two wrong judgments can occur.  
```
1. The door deny the registered fingerprint (=FN)  
2. The door approve the unregistered fingerprint (=FP)   
```

'Case 2' is more **_DANGEROUS_**. An outsider could break into our house.  
Therefore, you must determine the threshold at which FP does not occur.  
<img src = "https://user-images.githubusercontent.com/65939621/85498391-8e3d2c00-b61a-11ea-8ab3-7fb2f66e8a48.PNG" width="500">  

If you want to know more, this [video](https://youtu.be/4jRBRDbJemM) will be helpful for you.  
