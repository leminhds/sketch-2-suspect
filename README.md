# Sketch-2-Suspect using Pix2Pix

This project attemps  to use [Pix2Pix](https://phillipi.github.io/pix2pix/) model to tackle the sketch to image challenge. The code in this project is greately inspired by [Tensorflow Pix2Pix example](https://www.tensorflow.org/tutorials/generative/pix2pix). To those who are new to Pix2Pix, or GAN models in general, I highly recommend these resources.

The data used for the model are from [CUHK Face Sketch database](http://mmlab.ie.cuhk.edu.hk/archive/facesketch.html). The link also provide links to other relevant database. If you have access to those extra data, I would highly recommend you to mix the data to overcome some of the shortfall of our current output, which I will go into more details later.
CUHK dataset contains 188 pairs of sketches and faces, separated into 88 training data and 100 testing data. 

More data could also be obtained via [Image Analysis and Biometrics Lab](http://iab-rubric.org/resources/sketchDatabase.html). I am currently waiting to receive the access to the database.



## Conclusion and Improvement points
We have effectively leverage the Pix2Pix Model to map from a sketch to an image with visible similarities to the ground_truth image. A few drawbacks of our current work:
- First and foremost, the data. Due to lack of freely available data, we have only trained the model on data of Chinese University of Hong Kong (CUHK)'s students. Therefore, there is a lack of diversity of ethnicity and age group. We could therefore look for more data to improve the model
- All of the sketches are arguable of very similar style. Therefore, with different drawing style, we can imagine that our model will perform much poorer. This relates back to the lack of diversity in the dataset
- Lastly, about the model itself, we could try to replace the U-Net with ResNet model, for potential improvement
