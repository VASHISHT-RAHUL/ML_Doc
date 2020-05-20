### Why can’t we use backpropagation in “hard attention” but we can use it normally in “RELU” function and max-pooling without any problems?

- The maximum operator, used in relu and max pooling, is differentiable almost anywhere. the derivative of max(x, 0) is 1 if x>0 and else 0: when you petrubate the value of the maximum element a little, the maximum value changes linearly. The argmax operator that is used in hard attention, on the other hand, has a derivative of zero almost anywhere: when you petrubate the value of the maximum element a little, the index of the maximum doesn't change.
