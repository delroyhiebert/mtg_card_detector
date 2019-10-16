# Magic: The Gathering Card Detector

MTG Card Detector is a real-time application that can identify Magic: The Gathering playing cards from either an image or a video. It utilizes various computer vision techniques to process the input image, and uses [perceptual hashing](https://jenssegers.com/61/perceptual-image-hashes) to identify the detected image of the cards with the matching cards from the database of MTG cards. Refer to [opencv_dnn.py](https://github.com/hj3yoo/mtg_card_detector/blob/master/opencv_dnn.py) for more detailed implementation.

Initially, the project used a powerful neural network named ['You Only Look Once (YOLO)'](https://arxiv.org/pdf/1506.02640v5.pdf) to detect individual cards, but it has been removed as of Oct 12th, 2018 [(note)](docs/initial_dev_notes.md#oct-12th-2018) in favour of classical CV techniques. 

**Demo:**

[![Demo #1](https://img.youtube.com/vi/BZkRZDyhMRE/0.jpg)](https://www.youtube.com/watch?v=BZkRZDyhMRE "Demo #1")

**Demo:**

[![Demo #2](https://img.youtube.com/vi/kFE_k-mWo2A/0.jpg)](https://www.youtube.com/watch?v=kFE_k-mWo2A "Demo #2")