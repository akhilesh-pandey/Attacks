# JSMA

##<p>Jacobian Based Saliency Map Attack</p>

### This is an implementation of the paper "The Limitations of Deep Learning in Adversarial Settings."


I used a MLP with three hidden layers to train for hand written digit recognition on MNIST dataset.

The implementation consists of three step:
Step 1: Compute gradient of logit layer or softmax layer w.r.t the input pixels. This gives us Jacobian matrix.
Step 2: Using the jacobian computed in the step 1, compute saliency map. Saliency map tells us which pixels are going 
       the influence more in changing the the source class compared to the others.
Step 3: Chose the pixels corresponding to the maximum saliency value and perturb tha pixel with amount theta.
Step 4: Repeat step 1-3 unitl the image's label is predicted as target class or maximum distortion values is reached.
