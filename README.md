# Bilinear Magic Meets CLIP: Unsupervised Learning in Pig Counting Scenario

Abstract: Pig counting is an important task in pig marketing and farming. Most of the existing methods use supervised object detection for counting. 
However, supervised pig counting relies heavily on expensive data labeling, especially in the dense counting scenario. 
To address this issue, we adopt the Contrastive Language Image Pre-training model (CLIP) for unsupervised pig counting, and we innovatively tailor the image encoder of CLIP and the loss function to make it more suitable for pig counting. Our method replaces CLIP's image encoder with a bilinear model combining ConvNeXt and ResNet50 backbones, while the pooling operation is performed via a multi-head attention module. We further reconstruct the loss function by using a multi-modal full-ranking loss which captures the intrinsic correspondence between text and image. During the training phase, we use ranking text prompts to match a set of size-sorted image patches, and we calculate the maximum of the upper and lower triangular ranking losses to achieve alignment between text and image, ensuring that the image encoder is fine-tuned. During the testing phase, the image is split into patches and each patch is mapped to the most appropriate count. The proposed model is tested on a dense pig counting dataset, and extensive experiments demonstrate that our method outperforms unsupervised state-of-the-art counting methods and achieves almost the same results as supervised state-of-the-art counting methods.

<p style="text-align: center">
    <img src="docs/train_phase.png"/>
    <br/>
    During the training phase, we use image patches and text prompts to generate a similarity map and compute the full-ranking loss to fine-tune the image encoder.
    <br>
    <img src="docs/test_phase.png"/>
    <br/>
    During the testing phase, the images are divided into four patches, and a simple filtering strategy is used.
</p>

<br/>

Code and models will be released soon!
