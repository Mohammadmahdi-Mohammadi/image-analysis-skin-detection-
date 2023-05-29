# image-analysis-skin-detection-
In this problem, we want to segment the skin areas in images. You are given thress datasets; the first(D1) is a dataset with three features (RGB values) and a target(is it skin or not); You use this dataset for the train. The second one(D2) consists of multiple images that you should segment the skin areas and generate skin masks (You use this dataset for the test). The third one(pratheepan) is for training in e-g.

a) With sufficient tries, train a Gaussian mixture model for binary classification with the first dataset(D1). Discuss selected values for function parameters. (You are allowed to use libraries)

b) Load the second dataset(D2) and using obtained GMM in the part a, classify the images` pixels into skin/not skin. Plot your result as the same dimension images.

c) Now, using the Bayes classifiers, repeat the last part. Compare the results. Which one has better performance? Explain your reasons.

d) In probability-based classifiers, playing with probability instead of the predicted labels can outperform. Using the trained Bayes classifier, generate a skin probability map for each test image(D2). Skin probability map composed of the probability of each pixel that can be skin.

e) We want to apply to be locality to skin detection task. For this purpose, you should generate a new dataset using "pratheepan" images. First, load images and generate skin probability maps(with above Bayes classifier that you tranied), then create a 12-D feature vector with the original label for each pixel following as 3 RGB values + value of probability for that pixel + 8 probability values for neighbors(assume zero for border pixels that have fewer neighbor)
In the end, you have a dataset with 12 columns for features, one for the target(0/1), and the count of all pixels in all training images as rows.

f) Calculate the correlation coefficient for the above dataset. Can you indicate the locality attribute in this result? Describe the correlation coefficient and its usage.

g) Train a logistic regression model for obtained dataset and evaluate it with D2. Plot your result as the same dimension images suach as part b. Based on given grad truth, calculate confusion matrix. Compare result with part (b).
