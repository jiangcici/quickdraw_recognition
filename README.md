# quickdraw_recognition
cnn network to identify between apple ,axe & cat quick draw

# 1. Task

  The recognition in doodle recognition project is performed by a classifier that takes the user input, given as a sequence of strokes of points in x and y, and recognizes the object category that the user tried to draw. Our main task is to receive a draw as an  input and to predict in the highest success rate what is drawn in it from a list of labels that we will train our algorithm over it.The labels are consist of 345 categories from different subjects like animals,food,furniture and more.

# 2. Approach

  We plan to build a RNN-based recognizer for this project. 

  The model will use a combination of convolutional layers, LSTM layers, and a softmax output layer to classify the drawings. The input is a drawing that is encoded as a sequence of strokes of points in x, y, and n, where n indicates whether a the point is the first point in a new stroke.  

  We plan to learn the tutorial in TensorFlow and then define our own estimator. Then we will try different classification function and compare the result.

# 3. Dataset

  The dataset that we will use is based on the Google Quick Draw Sketches. The Quick Draw Dataset is a collection of 50 million drawings across 345 categories, contributed by players of the game Quick, Draw!. Since our memory is limited we will only load to memory 5000 draws per category. The data to present the sketches are ndjson files separated by category. 

  To realize the dynamic recognition, this data set split the sketch matrix into strokes, each stroke has a pixel matrix, and the order of strokes is also the feature to train the model. We are going to process the data into 256*256 format and become easier to train the model. We would use 70% of them to train, and 30% of them to test.
