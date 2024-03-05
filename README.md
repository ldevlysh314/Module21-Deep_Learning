# Module21-Deep_Learning

After importing dependancies and data, the non-beneficial columns 'EIN' and 'NAME' were dropped.

Determined number of unique values in each column:
APPLICATION_TYPE 17
AFFILIATION 6
CLASSIFICATION 71
USE_CASE 5
ORGANIZATION 4
STATUS 2
INCOME_AMT 9
SPECIAL_CONSIDERATIONS 2
ASK_AMT 8747
IS_SUCCESSFUL 2.

APPLICATION_TYPE was analysed. Cut-off value was chosen and list of application types created.

CLASSIFICATION value was used binning.

Categorical data was converted to numeric with pd.get_dummies.

Data was split into features and target arrays. "IS_SUCCESSFUL" - target variable for the model with values 1 for yes and 0 for no.

COMPILE, TRAIN AND EVALUATE THE MODEL.


1st try:
hidden_nodes_layer1=10
hidden_nodes_layer2=15
Results: loss 0.54, accuracy 0.739.

As the 2nd attempt to increase accuracy, I added 3rd layer;
hidden_nodes_layer1=10
hidden_nodes_layer2=15
hidden_nodes_layer3=25
Results: same, loss 0.54 and accuracy 0.739.

For the 3rd attempt to improve accuracy, I swapped 1st and 3rd layers;
hidden_nodes_layer1=25
hidden_nodes_layer2=15
hidden_nodes_layer3=10
Running 3rd attempt didn't change the outcome. Results: same, loss 0.54 and accuracy 0.738.

