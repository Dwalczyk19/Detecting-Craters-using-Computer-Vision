### Detecting-Craters-using-Computer-Vision

How can we detect crater's on planets, the moons, and other celestial bodies in the solar system? 

There are so many interesting features that can be extrapolated from the surface of a planet or moon, including craters, scarps (steep cliff), ridges (long narrow elevated landform with slopes on either side), chaotic fractures (e.g: Europa), or possible orogeny. A more expansive version of this will instead be a Physics Informed Neural Network (PINN) to predict precise mechanisms, e.g: orogeny, and their potential outputs. 

## Model Descriptions
- YOLO - You only look once; essentially annotating images (e.g: object identification, segmentation) by identifying outputs by a bounding box. For craters the model can (a) predict on cratered vs non-cratered terrain, as well as differentiating between whether they are small, medium or large.
- CNN - strictly detecting on a FIXED IMAGE SIZE, different outputs like a normal NN.
- ResNet - utilizes skip-connections wherein neural-nodes are activated yet are not passed to their immediate connection, but instead skip certain nodes. This is an approach to minimizing the vanishing gradient problem but connecting higher-level features with deeper levels of the network increasing the robustness of the model, potentially.  


Step 1: 
- Literature Review. What has been done before? What models are available? What platform should be used for training since I'm using my CPU to train presently (due to imcompatability between most platforms and Radeon GPUs [evidently my only contains 512mb of storage so it wouldn't be too good anyways]).
- Initially using Google Colab and CUDA's platform to work with the "free" T4 GPU. In future versions, it might be more useful to SSH into a paid for GPU (or just get a valid workstation...except $$$).

Step 2: 
- Gain access to crater (and non-crater) images which are beautifully provided by NASA's HiRise imagery (Mars); Lunar Reconnaissance Orbiter; and [Roboflow](https://universe.roboflow.com/).
- Need to be annotated in a bounding box format for YOLO (image1.jpg with an accompanied image1.txt). For multi-step predictions (localization followed by classification).
- Apply PCA to see if any notable characteristics are present in the the training dataset. 
- ** Also are elevation models; wavelength imagery (hopefully processed because this usually takes several steps of spectra processing); and thermal readings (e.g: inertia) available? If so, for what planetary bodies can use them? **

Step 3: 
- (a) Primitive Model Creation: YOLO Model training on known datasets with annotations of just craters (no differentiation between small, medium, and large) -> validation/tuning -> testing.
- (b) More Advanced Model Creation: adding multiple channels into CNN tensors. Not sure how the YOLO works presently, but if you can include more channels into the images you train on for lo

Step 4: 
- Manually test on telescope imagery from Celestron Nexstar 4SE. Presently, the images are taken using my iPhone through the telescopes lense; this is because my sony alpha 5000 camera is not an SLR camera....


Literature: 

https://www.nature.com/articles/s44453-026-00036-x#data-availability 

https://towardsdatascience.com/the-math-behind-convolutional-neural-networks-6aed775df076/

https://arxiv.org/pdf/1611.01186
