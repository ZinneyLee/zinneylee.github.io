# Let's study about Data Science!

Hello, my name is Jane Lee.  
This is my HOMEPAGE! And I'm trying to share my **Knowledge** about *Data Science*.  
Then,,, Let's join!  

## ROC curve

First at all, I want to talk about **"ROC curve".**   
It's an indicator that evaluates AI that we made.  


### CONFUSION MATRIX  
Do you ever heard about **CONFUSION MATRIX**?  
It is the evaluation table and consist of TP, FP, TN and FN.  
Before we begin to study the confusion matrix in earnest, e need to know what "TP, FP, TN, FN" is.  
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
  

### Threshold
Thresholds are similar as **Base Point**.  
It divides data into "Positive" or "Negative".  
~~However, in my story, it would be easier to understand to think that it is a prediction of our AI.~~

There is a graph about some data.  
<img src = "https://user-images.githubusercontent.com/65939621/85392496-90ee4180-b586-11ea-9730-46caaeb513e6.PNG" width ="500">  

Depending on where you put threshold, Confusion Matrix's value also changes.  
(Because real result values are _already_ fixed in the graph.)  

So, there are so many Confusion matrix.

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
<img src = "https://user-images.githubusercontent.com/65939621/85402051-feee3500-b595-11ea-9630-41e87642237e.png" width="500">
