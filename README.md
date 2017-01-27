# helloworld-vidyo.io-ios
Simple video chat application using Vidyo.io on iOS

> For an instructional video detailing how to build this app, take a look at this [Blog Post](https://vidyo.io/how-to/build-mobile-video-chat-app-ios-minutes).

## Clone Repository
git clone https://github.com/Vidyo/helloworld-vidyo.io-ios.git

## Acquire Framework
1. Download the latest Vidyo.io iOS SDK package: https://static.vidyo.io/latest/package/VidyoClient-iOSSDK.zip
2. Copy the framework located at VidyoClient-iOSSDK/lib/ios/VidyoClientIOS.framework to the root directory of where this repository was cloned (i.e. parallel to this README.md file)

> Note: VidyoClientIOS.framework is available in SDK versions 4.1.5.x and later; for previous versions of the SDK, build using libraries and frameworks as described below.

## Build Project
1. Open the project VidyoIODemo/VidyoIODemo.xcodeproj in Xcode 8.0 or later
2. Connect an iOS device to your computer via USB
3. Select the iOS device as the build target of your application
4. Build and run the application on the iOS device

## Alternatively, Build Using Libraries & Third Party Frameworks
If preferred, you may create your project using a combination of libraries and third party frameworks, as opposed to the VidyoClientIOS framework.

1. Import the library and header directories from the Vidyo.io iOS SDK package into your project:
	* VidyoClient-iOSSDK/lib
	* VidyoClient-iOSSDK/include

2. Add the following libraries and frameworks to the Linked Frameworks and Libraries settings in the General settings of the target:
	* libVidyoClient.a	(included in Vidyo.io iOS SDK package)
	* libcrypto.a		(included in Vidyo.io iOS SDK package)
	* libopus.a		(included in Vidyo.io iOS SDK package)
	* libspeex.a		(included in Vidyo.io iOS SDK package)
	* libspeexdsp.a		(included in Vidyo.io iOS SDK package)
	* libsrtp.a		(included in Vidyo.io iOS SDK package)
	* libssl.a 		(included in Vidyo.io iOS SDK package)
	* VPX.framework		(included in Vidyo.io iOS SDK package)
	* AVFoundation.framework
	* CoreGraphics.framework
	* CoreVideo.framework
	* QuartzCore.framework
	* UIKit.framework
	* AudioToolbox.framework
	* CoreLocation.framework
	* Foundation.framework
	* Security.framework
	* CFNetwork.framework
	* CoreMedia.framework
	* OpenGLES.framework
	* SystemConfiguration.framework

3. In the Build Settings of the target, update the Framework Search Paths, Header Search Paths, and Library Search Paths to reference the directories imported in step 1.

