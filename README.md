# Hololens-ComputerVision

This project shows how to use windows [media capture](https://msdn.microsoft.com/library/windows/apps/windows.media.capture.mediacapture.aspx) in Hololens 2 to access the Camera, take picture send the image to a computer vision (CV) service and display an augmented reality asset close to where the picture was taken depending on the CV result.

For now the project is just a copy of Picture Sample working with latest Unity 2019.4.23f1, new XR plugin management and MRTK 2.6.1

Refer to [Locatable camera info from Microsoft](https://docs.microsoft.com/en-us/windows/mixed-reality/locatable-camera) for details on the Device Camera.

[Locatable camera in Unity](https://docs.microsoft.com/en-us/windows/mixed-reality/locatable-camera-in-unity) provides the key API and sample scripts.


### Dependencies
- Unity 2019.4.23f1
- Text Mesh Pro
- MRTK Foundation 2.6.1

### Install
Open the project in Unity 2019.4.23f1

Unity should ask to install Text Mesh Pro and should install the MRTK Libraries
- Text Mesh Pro via Window, Text Mesh Pro, install TMP Essential Resources
- MRTK Libraries via XR plugin management in Unity Project settings

Verify that ...
- your build settings is correctly set for Hololens 2 e.g. switch to Universal Windows Platform, ARM64
- The build contains the scene TakePictureScene (using Add Open Scenes)
- 'MixedRealitySpeechCommandsProfile' in CustomProfile folder contains the key word "Scan Image".

Build, deploy to Hololens 2 (through Visual Studio 19).

The App should request access to Camera and Microphone, accept !

Enjoy taking Picture by just saying "Scan Image"

### Next Steps
- Send the image to a Computer Vision service and display the result as an augmented reality asset close to where the picture was taken
