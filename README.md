# Exploration of ARKit

This is an exploration of ARKit for Prof. Tobias Hollerer's CS291A course at UC Santa Barbara.

## Links

- [Apple's Augmented Reality general website](https://developer.apple.com/augmented-reality/)
- [Apple's ARKit website](https://developer.apple.com/augmented-reality/arkit/)
- [Apple's SDK and Betas website](https://developer.apple.com/download/)
- [Tutorial from Ray Wenderlich](https://www.raywenderlich.com/737368-beginning-arkit)
- [RealityKit discussion on RayWenderlich](https://www.raywenderlich.com/books/apple-augmented-reality-by-tutorials/v1.0/chapters/9-realitykit)

## Creating an AR Project in Xcode

Creating AR projects in Xcode is fairly easy, assuming you have the latest version of Apple's software. The version this document is made with is Xcode 13.2.

First create a new project and choose Augmented Reality App:

![ChooseTemplate](images/ChooseTemplate.png)

Next you'll need to name your project and choose the technology you want to use. Apple offers 4 different technologies for rendering. The rendering technologies are discussed in [this Stack Overflow question](https://stackoverflow.com/questions/60505755/high-quality-rendering-realitykit-vs-scenekit-vs-metal).

The choices are:

- **RealityKit**—the newest technology, this is a high level sdk that enables many of the latest features like the use of the LiDAR scanner (and photogrammetry), ray-traced shadows, and multi-user support. It is not as customizable as SceneKit, but offers more features out of the box that are likely of interest to AR developers.
- **SceneKit**—this is Apple's 3D technology conceived for VR and 3D games. While SceneKit is older, it does offer [some functionality that is not available in RealityKit](https://medium.com/geekculture/the-top-9-most-in-demand-features-for-realitykit-3-0-c1a50f08909d). It is highly customizable, but has not been updated since 2017.
- **SpriteKit**—this is Apple's 2D game framework.
- **Metal**—this is Apple's low-level 3D framework for generating geometry very quickly. Metal underlies many graphics API's already. Metal shaders are written in C++. Metal should be considered when performance is critical.

![ChooseTechnology](images/ChooseTechnology.png)

## The RealityKit Demo Project

