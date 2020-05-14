# The #mood project

Map your facial expression to an iconic Soraya Montenegro meme using machine learning. 

The application consists of 3 parts:

1) The FaceOSC program. It sends 132 /raw inputs to Wekinator on port 8338

2) The Wekinator project. It takes the 132 /raw inputs and trains 1 output of
type classifier with 4 classes. Class 1 is trained on the neutral expression,
class 2 on smiling, Class 3 is a surprised expression and class 4 an angry
one. I used a classifier instead of continuous outputs because it was quicker
to train.

3) A Pure data patch. It reads from wekinator on port 7005 one output, the class
number. According to the class it displays the equivalent meme of Soraya
Montenegro.
