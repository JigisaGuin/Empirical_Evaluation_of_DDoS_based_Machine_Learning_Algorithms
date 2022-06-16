# Empirical_Evaluation_of_DDoS_based_Machine_Learning_Algorithms
In this project, we have focussed on detecting DDoS attacks using five different Machine Learning models. We have considered the CIC-IDS 2017 dataset for the purpose.CIC-IDS2017 dataset contains benign and the most up-to-date common attacks, which resembles the true real-world data.

## Procedure
All the provided datasets are merged and a single dataset is formed with a large dimension. The data is sampled out into different set to consider the analysis based on the dataset size. We have also considered a comparison different number of important features to evaluate the models. The dimension of the dataset is quite large, hence optimizing the size of the dataset, by removing the irrevalent features, is necessary for a good performance. We have performed feature selection using Random Forest Classifier and considered conditions based by sampling out the 10, 20 and 30 important features respectively. On this reduced dataset we trained, validated and tested five Machine Learning models namely K-Nearest Neighbor, Logistic Regression, Decision Tree, Gaussian Naive Bayes and Support Vector Machine. We analyzed the respective accuracy results of performance of each of the model. As for sampling out the number of rows of the dataset, we have considered three sample set, namely 25000 , 50000 and 100000 samples, and accuracy of the models are examined for each of the sample set by the above procedure. 

For most of the cases KNN gave the best results. Performance of all other models were satisfactory.To increase the overall performance we considered two different approches.

## Majority Vote
We use the technique of majority voting to check if accuracy of the approach can be further increased. We merge or concatenate the predicted output of the models from the previous phase and assign ‘1’ if there are a greater number of 1’s than 0’s for each row and similarly assign a ‘0’ if there are a greater number of 0’s than 1’s for each row. We perform this for all the rows in the dataset and name the column ‘majority’. Now we predict the accuracy of the approach by calculating the accuracy score between the ‘majority’ column and the test set. We test by combining different sets of the ML models like the average performing models with the best performing ones, or the worst performing models with the ones with moderate performance and so on. We observed their performance and found conclusions for each set of sampling of the dataset.

## Blending Approach
We have also followed blended method where a combination of the selected models are used to create a blended dataset. We use this dataset to train and validate the models and then predict using the Random Forest Classifier model. In this blended approach, we have considered various combinations of the five models used earlier to conclude on the performance rate of the models. For different sampling of the dataset, blending approach often provides the best results by giving more than a 90% accuracy. After examining all the different sampling of the dataset, we came to the conclusions on the models performing best in each of the situation, with increasing number of features as well as the size of the dataset.


#### Bi-Class Evaluation
We have also observed the performance of the models as well as the approaches on a Bi-class dataset.
