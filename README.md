# MC-CNN-python3 implementation
Rewrite from Jackie-Chou's python2 version(https://github.com/Jackie-Chou/MC-CNN-python)

simple implementation of MC-CNN origined from the paper[1] in python

### environment requirements
1. python 3.6
2. tensorflow >= 1.4
3. numpy >= 1.14.0
4. cv2 >= 3.3.0
5. tqdm >= 4.24.0

### file description
- model.py: MC-CNN model class. Only the fast architecture in [1] is implemented but I suppose it's not hard to build the accurate one.
- datagenerator.py: training data generator class. This is used to generate data for model training.
- train.py: training of MC-CNN.
- util.py: some helper functions such as parsing calibration file.
- process_functional.py: processing functions used in stereo matching such as cross-based cost aggregation.
- match.py: main program of stereo matching. Call relevant procedures from process_functional.py by order and save the final results as [Middlebury stereo dataset(version 3)](http://vision.middlebury.edu/stereo/submit3/) required.

### usage
1. train the MC-CNN model. This is pretty quick on my Nvidia 1080Ti GPU for 2000 epochs.
for details type
> python train.py -h

2. use trained model and do stereo matching. This is time-consuming.
for details type
> python match.py -h

### License
MIT license.

### Reference
[1] Jure Zbontar, Yann LeCuny. *Stereo Matching by Training a Convolutional Neural Network to Compare Image Patches*
