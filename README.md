# Sensor-based-Hand-Gesture-Recognition-using-Deep-Learning
# Abstract
This study seeks to evaluate the performance of deep learning algorithms, namely convolutional neural network (CNN) and recurrent neural network (RNN), as well as a hybrid model between the two, on the SmartWatch hand gestures dataset provided by the TeV website. We conducted several experiments to implement CNN, LSTM, and hybrid CNN-LSTM and optimize their parameters on the target dataset. Our findings indicate that all three models achieved an average accuracy of 95%, demonstrating promising results for this research. The hybrid CNN-LSTM model performed slightly better than the others, with an accuracy of 96%. Lastly, we suggested potential future directions and areas for further research in this field. the Structure of the sensor-based hand gesture recognition system that we will apply.

![image](https://user-images.githubusercontent.com/94287604/221333788-fc838ecd-929d-4d12-96b2-cc2d88337f12.png)


# Dataset
In this project, the dataset used is the [hand gesture dataset](https://tev.fbk.eu/resources/smartwatch) from TeV Technologies of Vision. The dataset was collected using the accelerometer sensor in the first-generation Sony smartwatch and includes 20 gestures performed by 8 different users. The dataset is organized into eight user folders, each containing 20 subfolders for each gesture. Each subfolder includes 20 instances of the gesture performed by the user. To simplify the analysis and management of the dataset, the dataset files have been consolidated into a single .txt file, which can be found as the "hand_gesture_dataset.txt" file in this GitHub repository.

# Data Pre-processing

## Data Splitting:
The data was split 80/10/10 into training, validation, and testing sets. This allows for adequate training data while reserving data for evaluation and preventing overfitting.

## Data segmentation experiment:
To choose a suitable window size and overlapping ratio for the hand gesture dataset, an experiment was conducted. Window sizes of 5 to 200 were tested based on the range of rows for each gesture, and overlapping ratios of 0%, 25%, 50%, and 75% were also tested. The experiment was conducted on two models, CNN and LSTM.

![image](https://user-images.githubusercontent.com/94287604/221333529-e8c22d03-e631-47a4-a6b5-039d95474f03.png)

The experiment showed that higher overlapping ratios, particularly 75%, led to better performance in both the CNN and LSTM models across all tested window sizes. In addition, the window size was chosen is 50.

A hybrid CNN-LSTM structure is used to combine the strengths of both models, where the CNN extracts features and the LSTM performs classification. The hybrid model is constructed by combining the CNN and LSTM models.

![image](https://user-images.githubusercontent.com/94287604/221333569-c26b1fae-8524-4894-9dcb-57e5331c8f81.png)


# Results:
The table shows how well the CNN, LSTM, and CNNLSTM models performed on new and unseen data from the test set, as measured by their test accuracy and loss values. Test accuracy indicates how good the models are at recognizing new data, while loss measures the difference between the predicted and actual outputs. Lower loss values mean better performance, and are associated with higher accuracy.

![image](https://user-images.githubusercontent.com/94287604/221333599-fdb76087-d601-4039-b1b5-8edbe597fe16.png)




