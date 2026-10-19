# Detecting-Craters-using-Computer-Vision

How can we detect crater's on planets, the moons, and other celestial bodies in the solar system? 
Step 1: 
- Literature Review. What has been done before? What models are available? What platform should be used for training since I'm using my CPU to train presently (due to imcompatability between most platforms and Radeon GPUs [evidently my only contains 512mb of storage so it wouldn't be too good anyways]).

Step 2: 
- Gain access to crater (and non-crater) images which are beautifully provided by NASA's HiRise imagery (Mars); Lunar Reconnaissance Orbiter; and [Roboflow](https://universe.roboflow.com/).
- A consistent data format has to be provided, likely .jpg.
- Also are elevation models; wavelength imagery (hopefully processed because this usually takes several steps of spectra processing); and thermal readings (e.g: inertia) available? If so, for what planetary bodies can use them?

Step 3: 
- Model creation.
- Training - validation - tuning - and testing.

Step 4: 
- Manually label my own personal imagery from Celestron Nexstar 4SE, and test using either a personally trained model or pre-trained model.


Literature: 
https://www.nature.com/articles/s44453-026-00036-x#data-availability 
https://towardsdatascience.com/the-math-behind-convolutional-neural-networks-6aed775df076/
