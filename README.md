# Module_14_HW
Module 14 Challenge assignment

In this module we built a trading bot and used historical data to test the success of our model and how well it might predict future results.
In the first iteration of this model we created a DMAC model to find when a short moving average (4 days) crossed through a longer moving average
(100 days) to generate buy signals. Below we see the results of our algo.  Our model is good at predicting buy signals but suffers when predicting
sell signals as evidenced by the lower precision when looking at -1 (our sell signal). The recall is very low as is the F1 score. 
![Screen Shot 2023-02-16 at 7 28 26 PM](https://user-images.githubusercontent.com/117240889/219535599-90ab024e-5234-403e-95ea-0f0c5abcdb94.png)
![Screen Shot 2023-02-16 at 7 28 38 PM](https://user-images.githubusercontent.com/117240889/219535626-bd06cc70-77c4-4b44-ab36-b67a0e4f69bb.png)

For the next iteration of the algo I chose to use AdaBoostClassifier to test the model for predictive power. The reason I chose this is because the 
classifier adjusts the weights of incorrectly classified values so there is greater emphasis on more difficult classification instances. Below are
the results of this AdaBoost model on the same data set. 
![Screen Shot 2023-02-16 at 7 28 54 PM](https://user-images.githubusercontent.com/117240889/219536650-97d90176-ccc3-40f7-8196-e7f014a7e542.png)
![Screen Shot 2023-02-16 at 7 29 03 PM](https://user-images.githubusercontent.com/117240889/219536698-b40571bc-34d6-4e22-a8f3-c58d7cd2c16f.png)

We can see that the AdaBoost classifier somewhat improved our models predictive power. Precision in detecting sell signals improved slightly as 
well as our recall and F1 scores. Additionally this model had slightly better returns than our original model. 

In conclusion, our AdaBoost model slightly outperformed the SVM model in both predictive power and strategy returns. 
