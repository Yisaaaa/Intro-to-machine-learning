# [What is Model Validation](https://www.kaggle.com/code/dansbecker/model-validation)

When we build model, we wanna know if our model's predictions are actually accurate. A common mistake many people make is use the training data to validate the accuracy of their model. 

The problem with this is that it would not give us an accurate prediction. "But when I try it, it's pretty much very accurate?" Exactly. The training data appears accurate because it is derived from that same data. If we were to use it on other data our model hasn't seen before it would look inaccurate.

When we measure model quality, we first want to translate it in an understandable way. If you compare 10, 000 houses with their actual value and predicted value, you will likely find a mix of good and bad predictions. But looking through a list of 10, 000 houses and comparing them would be pointless, what does it even mean? That's why we need to have a metric and summarize our model based from that metric

## Mean Absolute Error (MAE)

There are many metrics for summarizing model quality but we will start with what we call **Mean Absolute Error** or **MAE**.

With MAE, we look for how much is the error in our predicted data vs actual data.

```
error = actual - predicted
```

We have to convert our error into its absolute value so they become positive. Now for every prediction we take their error value and average all of them. Hence we can then say:

```
Our model is off by x on average

where: 
	x is the average error
```

