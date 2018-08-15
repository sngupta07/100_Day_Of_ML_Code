<pre>
Approach
# Programming Language: Python
# Tools used
1.	Numpy
2.	Pandas 
3.	Matplotlib
4.	Scikit-learn
# Steps (Data processing) 
1.	I read the data using pandas. 
2.	Merged all the data on building Id, ward Id, district Id, vdcmun Id (left join) 
3.	Full null values with - 999 because it not affect the dataset and also not show any null values present. 
4.	Use label encoder to encode the categorical features. 
5.	After I dropped the building_id from the test and train dataset because there is no need of that. 
# Steps (Machine learning modeling) 
1.	I split the train dataset in training and validation set. 
2.	Use various ml models but no one gave me better result. 
3.	Then I tried Xgboost with some hyperparameters like learning rate, max depth, Subsample, objective, loss function, etc. When I train the model, it took time but gave me better result than the previous models I used. 
4.	For more accuracy I used Lightgbm with the same hyperparameters but there is no improvement in result. 
5.	Then I tried with Lightgbm again with KFold split and 5 CV but again it also not give result with significant improvement. 
6.	Then at last I tried with cat boost with hyperparameters learning rate, max depth, objective. Then it gives the better result than the previous one. 
# Overall Conclusion 
Import dependencies - > Read the dataset - > Data preprocessing - > Splitting dataset in training and validation set - > Apply Cat boost ml model - > Result 

Overall Weighted F1 score: 0.785
</pre>
