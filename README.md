# Pneumonia detection from chest x ray images using transfer learning on Inception v3 using tensorflow and keras.

## Transfer learning, huh what's that ?
  - The name suggests that some kind of knowledge is transferred to solve something. In ml this knowledge is acquired by an algorithm by drawing inferences from a dataset. Well datasets are huge and training on them takes time and computation power which isn't easy for common folks like us. So what we do is, we select a pretrained model like **Inception-v3** which has been trained on massive data and can classify images into 1000 classes. This model however cannot detect pneumonia from chest x ray images. So we get the data of chest x ray images, normal and pneumonia ones and retrain it to detect pneumonia. Ergo the name transfer learning.

## Plan
  - Explore dataset (https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia)
  - Load inception model
  - Add custom layers for to detect pneumonia (This part needs exploration). At the current stage we exactly don't what layers should be added like how deep and wide and what will be it's effects. 
  - We will also some cool training helpers like ModelCheckpoint, EarlyStopping, ReduceLROnPlateau
  - Measure performance
  - Celebrate
  
## Performance of the trained model

```
------------------------------------------------------------------------------------------
Precision     : 95.61%
Recall        : 78.21%
F1-Score      : 86.04%
------------------------------------------------------------------------------------------
```

## Examples

  - Normal detected as normal
  - ![alt text](https://github.com/a1rishav/pneumonia_detection_from_chest_x_ray/blob/master/images/normal.png)
  
  - Pneumonia detected as normal
  - ![alt text](https://github.com/a1rishav/pneumonia_detection_from_chest_x_ray/blob/master/images/pneumonia.png)
