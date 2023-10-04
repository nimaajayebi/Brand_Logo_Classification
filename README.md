# Brand_Logo_Classification
Brand Logo Classification with CNN, SVM and transfer learning

The project was to develop a brand logo classification model. To achieve this goal, various machine learning models were tested from simple models to more advanced complicated models. The first step was to utilize support vector machine (SVM) and naïve bayes (NB) classifiers. Even though they were helpful in achieving insight into deciding between using HiPerGator or personal laptops, the model’s accuracy was not acceptable. Even after implementing principal component analysis (PCA) the accuracy didn’t go beyond 47 percent. In the next step, convolutional neural networks (CNNs) were tested to achieve better results. This included testing different layers for the network, and adding dropouts and regularizers. Yet, the resulting accuracy which was 59 percent wasn’t satisfactory. After some exploration, the team concluded that employing transfer learning was the most suitable approach for image classification, and hence the optimal choice for this particular undertaking. This included utilizing different pre-trained models, unfreezing different numbers of layers and adding regularizers to the model. All these efforts led to a satisfactory accuracy of 90 percent. Overall, this project helped the team to implement the methods that were taught in the class, in a project to have a better understanding of those methods.
------------------
# Final Project - Submission

Here are two files : 
1. EEL5840-Project_Train_function_FINAL.ipynb
2. EEL5840-Project_Test_function_FINAL.ipynb

Libraries:
The following libraries are used in this project, so please have them installed in your system:
* tensorflow
* keras
* statistics
* sklearn

_____________EEL5840 - Project-Train_function_____________

function call :  
train(training_file, label_file, D = 150)

Inputs:
* training_file => "data_train.npy"
* label_file => "t_train.npy"
* D = 150 => Dimensions for cv2 reshape from 300x300 to 50x50

Saving the model: (Will be done during function call)
model.save("ECE_saved_model.md")

Output:
* Average training and validation accuracy plot
* Avergae training and validation loss


_____________EEL5840 - Project_Test_function:_____________

function call : 
test(X_test, t_test, D = 150)

Inputs:
* X_test => "YOUR TEST DATA.npy"
* t_test => "YOUR TEST LABELS.npy"

You should add the path of your Test Data and Test Labels in the place of the above-mentioned 
Output:
* Classification Report
* Confusion Matrix
