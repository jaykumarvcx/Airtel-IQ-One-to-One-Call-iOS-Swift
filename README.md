# One-to-One Video Call using Swit and Airtel IQ for iOS

This client application written in Swift demonstrates how you can implement video calling capabilities in your mobile applications using Airtel IQ Toolkit. The application runs on an iOS device and utilizes Airtel IQ iOS SDK to conduct an RTC session. The sequential tasks performed by the client application to conduct an RTC session are as given below:  

* Fetch token from the application server. 
* Connect to the room using the received token. 
* Publish media streams in the room. 
* Subscribe to remote media streams in the room. 
* Observe and handle session-related events. 

The sample application demonstrates the following advance features along with basic video call: 

* Mute/Unmute audio. 
* Mute/Unmute video. 
* Switch Camera (front or rear). 
* Switch to Speaker. 
* Disconnect. 


## 1. Getting Started

### 1.1 Pre-Requisites

#### 1.1.1 Authorization Credentials

Follow the steps given below to generate API Credentials required to access Airtel IQ: 

* [Create a free account on Airtel IQ](	https://portal.videoiq.airtel.in/cpaas/trial-sign-up/)  
* Create your Project 
* Get the App ID and App Key generated against the Project. 

#### 1.1.2. Requirement: 

* An iOS Device to test the sample application as a simulator/emulator does not support playing video or publishing a local Stream. 

* iOS Deployment Target: 10.0 or higher
Xcode Version: 10.0 or higher
Language: Either Swift or Objective-C
Swift Language Version: 3.0 or higher
Objective-C: In Compliance with iOS 10.0+

#### 1.1.3 Configure iOS Client 

* Open the App
* Go to WebConstants and change the following:
``` 
 /* To try the App with Airtel IQ Hosted Service you need to set the kTry = true, when you setup your own Application Service, set kTry = false  */
     
     public  static  final  boolean kTry = true;
     
 /* Your Web Service Host URL.  The following host is applicable when kTry = true */
 
     String kBaseURL = "https://demo.videoiq.airtel.in/"
     
 /* Your Application Credentials are required to try with Airtel IQ Hosted Service. You can remove these when you setup your own Application Service */
     
     String kAppId = ""  
     String kAppkey = ""  
 ```

#### 1.1.4 Sample application server 

Once you have downloaded the client code, you need to download the server code to provision video room on Airtel IQ server. Use any of the Repositories listed below to setup your application server: 

* Laravel 
* PHP 
* Nodejs 
* Python 
* C# 

Clone or download a repository of your choice and configure the server as per the instructions given in the respective README document.  

To directly try the sample code without having to configure an application server, you can also use the Airtel IQ test server as explained in section 2. However, it is recommended to configure your own application server to build a multiparty video calling web app. 

 

### 1.2 Test

* Open the App in your device.  
* A Form to enter the Name and Room ID opens. 
* Create a Room by clicking on “Create Room” button. 
* Use the Room ID to enter the Room as a Moderator or a Participant and share the Room ID with others who want to join the RTC session in the Room. 
* You are now in a video call with others, who have joined the same room. 

Note: This sample application creates a virtual room with limited Participants and 1 Moderator for demonstration purposes. 
  
## 2. Pre-configured Test Server 

As mentioned in section 1.1.4 above, you have an option to run your client application on [Airtel IQ pre-configured environment](https://try.videoiq.airtel.in) instead of setting up your own application server.  

This allows you to quickly test the performance of Airtel IQ video calls before getting into the development of your application.  

As the Airtel IQ test server has been configured for demonstration purpose only, it only allows to: 

* Conduct a single session with a duration lesser than 10 minutes. 
* Host a multiparty call with less than 3 participants. 

Refer to the [Demo App Server](https://developer.videoiq.airtel.in/video/sample-code/#demo-app-server) for more information.   

Once you have successfully tested your application on the test server, you can set up your application server as explained in section 1.1.4 above. ## 3 iOS Toolkit

## 3. Know more about Client API 

The client APIs are called from the Airtel IQ iOS SDK (nxRTCiOS.framework) which runs in the client application. The client APIs are used to communicate with the Airtel IQ video services and monitor the client-side state of the RTC session.  

The client APIs are typically used to: 

* Connect to the desired room using the token received from the application server 
* Manage local audio and video 
* Handle room and stream related events initiated by the user 

The client APIs handle four major entities: 

* Airtel IQ Room: It handles room/session related events like connection, local stream publication, and remote stream subscription. 
* Airtel IQ Stream: It identifies audio/video/data stream published by the user. 
* Events: It represents the events related to the room and the stream. 
* Player: It represents the customizable UI element used to render the audio/video stream in the DOM. 

In addition to the features demonstrated in this sample program, the SDK has many helpful APIs available for the developers to utilize like: 

* Text chat 
* Session recording  
* File sharing 
* Screen sharing 
* Streaming 
* Annotation 
* Canvas 

And many more such exciting features. 

Read [iOS Toolkit Documentation](https://videoiq.airtel.in/developer/video-api/client-api/ios-toolkit/) for more details.  

Download [iOS Toolkit](https://videoiq.airtel.in/developer/wp-content/uploads/IOS_SDK_1.9.4/EnxRTCiOS.framework_1.9.4.zip) to get the latest version of iOS SDK. 

## 4. Support

Airtel IQ provides a library of Documentations, How-to Guides, and Sample Codes to help software developers, interested in embedding RTC in their applications. 

Refer to the [Complete Developer’s Guide](https://developer.videoiq.airtel.in/) for more details. 

You may also write to us for additional support at [support@AirtelIQ.io.](mailto:support@videoiq.airtel.in) 
