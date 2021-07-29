## Third party libraries used by BeLive iOS SDK

### Viewer

**Viewer only**

> Live stream libraries are not required if HLS playback is preferred. It is omitted from this document.

```bash
#MARK: - Network
pod 'Alamofire', '4.9.1'
pod 'AlamofireObjectMapper', '5.2.1'
pod 'SDWebImage', '5.11.0'

#MARK: - Chat - in-House (gRPC)
pod 'SwiftGRPC', '0.11.0'
pod 'gRPC', '1.24.2'
pod 'pop', '1.0.12'

#MARK: - Chat - Agora RTM
pod 'AgoraRtm_iOS', '1.4.3'

#MARK: - Util - For UI
pod 'ObjectMapper', '3.5.3'
pod 'PromiseKit', '6.13.1'
pod 'IQKeyboardManagerSwift', '6.5.6'
pod 'Toast-Swift', '5.0.1'
pod 'SnapKit', '5.0.1'
pod 'SVProgressHUD', '2.2.5'
pod 'SwiftyPlistManager', '1.0.2'

#MARK: - Reactive extensions - Rx
pod 'RxSwift', '5.1.2'
pod 'RxCocoa', '5.1.1'
pod 'RxRelay', '5.1.1'
pod 'RxAppState', '1.6.0'
pod 'RxReachability', '1.1.0'

#MARK: - License - CryptoSwift
pod 'CryptoSwift', '1.3.8'
```

### Network and Image Loading

```bash
#MARK: - Network
pod 'Alamofire', '4.9.1'
pod 'AlamofireObjectMapper', '5.2.1'
pod 'SDWebImage', '5.11.0'
```

Alamofire is an HTTP networking library written in Swift. BeLive SDK uses Alamofire to communicate with RESTful APIs of BeLive backend servers.

- Official Alamofire Github : https://github.com/Alamofire/Alamofire
- Official Alamofire License : https://github.com/Alamofire/Alamofire/blob/master/LICENSE

AlamofireObjectMapper is an Alamofire extension which converts JSON response data into swift objects using ObjectMapper. BeLive SDK requires AlamofireObjectMapper to process API responses.

- Official AlamofireObjectMapper Github : https://github.com/tristanhimmelman/AlamofireObjectMapper
- Official AlamofireObjectMapper License : https://github.com/tristanhimmelman/AlamofireObjectMapper/blob/master/LICENSE

SDWebImage is an asynchronous image downloader with cache support as a UIImageView category. BeLive SDK requires SDWebImage to process image resources.

- Official SDWebImage Github : https://github.com/SDWebImage/SDWebImage
- Official SDWebImage License : https://github.com/SDWebImage/SDWebImage/blob/master/LICENSE

### Real-time chat

BeLive has developed in-house chat based on gRPC. We have an alternative option for chat which is developed using Agora RTM SDK. Depending on use case, we can enable and package one of the chat platform with SDK.

_In-house chat_

```bash
#MARK: - Chat - in-House (gRPC)
pod 'SwiftGRPC', '0.11.0'
pod 'gRPC', '1.24.2'
pod 'pop', '1.0.12'
```

In gRPC, a client application can directly call a method on a server application on a different machine as if it were a local object, making it easier for you to create distributed applications and services. BeLive in-house chat feature is dependent on the gRPC framework.

- Official gRPC Github : https://github.com/grpc/grpc-swift
- Official gRPC License : https://github.com/grpc/grpc-swift/blob/main/LICENSE

_Agora Chat_

```bash
#MARK: - Chat - Agora RTM
pod 'AgoraRtm_iOS', '1.4.3'
```

Agora is a RTM (Real-time Messaging) SDK used to send and receive messages. Agora is required for alternative implementation of real-time chat feature.

- Official Agora RTM site : https://docs.agora.io/en/Real-time-Messaging/messaging_ios?platform=iOS

> Note : Agora is a paid service

### Utility Libraries for iOS

```bash
#MARK: - Util - For UI
pod 'ObjectMapper', '3.5.3'
pod 'PromiseKit', '6.13.1'
pod 'IQKeyboardManagerSwift', '6.5.6'
pod 'Toast-Swift', '5.0.1'
pod 'SnapKit', '5.0.1'
pod 'SVProgressHUD', '2.2.5'
pod 'SwiftyPlistManager', '1.0.2'
```

ObjectMapper converts your model objects (classes and structs) to and from JSON. BeLive SDK requires ObjectMapper to process API responses.

- Official ObjectMapper Github: https://github.com/tristanhimmelman/ObjectMapper
- Official ObjectMapper License : https://github.com/tristanhimmelman/ObjectMapper/blob/master/LICENSE

PromiseKit implements Promises for Swift & ObjC. PromiseKit is used for asynchronous programming in BeLive SDK.

- Official PromiseKit Github: https://github.com/mxcl/PromiseKit
- Official PromiseKit License: https://github.com/mxcl/PromiseKit/blob/master/LICENSE

IQKeyboardManagerSwift is a codeless drop-in universal library which prevents issues of keyboard sliding up and cover UITextField/UITextView. IQKeyboardManagerSwift is used for handling of keyboard in chat UI in BeLive SDK (smart keyboard).

- Official IQKeyboardManagerSwift Github: https://github.com/hackiftekhar/IQKeyboardManager
- Official IQKeyboardManagerSwift License: https://github.com/hackiftekhar/IQKeyboardManager/blob/master/LICENSE.md

Toast-Swift is a Swift extension that adds toast notifications to the UIView object class. Toast-Swift is used to implement toast notification in BeLive SDK.

- Official Toast-Swift Github: https://github.com/scalessec/Toast-Swift
- Official Toast-Swift License: https://github.com/scalessec/Toast-Swift/blob/master/LICENSE

SnapKit is a DSL (Domain Specific Language) to make Auto Layout easy on both iOS and OS X. SnapKit is used to support Autolayout by code in BeLive SDK.

- Official SnapKit Github: https://github.com/SnapKit/SnapKit
- Official SnapKit License: https://github.com/SnapKit/SnapKit/blob/develop/LICENSE

SVProgressHUD is a clean and lightweight progress HUD for your iOS and tvOS app. SVProgressHUD is used to display progress on UI in BeLive SDK.

- Official SVProgressHUD Gitbub: https://github.com/SVProgressHUD/SVProgressHUD
- Official SVProgressHUD License: https://github.com/SVProgressHUD/SVProgressHUD/blob/master/LICENSE

SwiftyPlistManager is a lightweight plist data management framework for iOS 10.3+. SwiftyPlistManager is used for plist data management to manage SDK configurations.

- Official SwiftyPlistManager Github: https://github.com/rebeloper/SwiftyPlistManager
- Official SwiftyPlistManager License : https://github.com/rebeloper/SwiftyPlistManager/blob/master/LICENSE

### Reactive Extensions (Rx)

```bash
#MARK: - Reactive extensions - Rx
pod 'RxSwift', '5.1.2'
pod 'RxCocoa', '5.1.1'
pod 'RxRelay', '5.1.1'
pod 'RxAppState', '1.6.0'
pod 'RxReachability', '1.1.0'
```

RxSwift is used for reactive programming in iOS platforms. Async tasks are implemented via Reactive Extensions (Rx) dependencies in BeLive SDK.

- Official Rx Github: https://github.com/ReactiveX/RxSwift
- Official Rx License : https://github.com/ReactiveX/RxSwift/blob/main/LICENSE.md

### License (CryptoSwift)

```bash
#MARK: - License - CryptoSwift
pod 'CryptoSwift', '1.3.8'
```

CryptoSwift is a library of crypto related functions and helpers for Swift implemented in Swift. CryptoSwift is used for license verification of SDK.

- Official CryptoSwift Github: https://github.com/krzyzanowskim/CryptoSwift

- Official CryptoSwift License : https://github.com/krzyzanowskim/CryptoSwift/blob/master/LICENSE

### Appendix

In case of `non-HLS playback such as RTMP, FLV etc.`, BeLive SDK uses KSYMediaPlayer.

- Official KSYMediaPlayer Github : https://github.com/ksvc/KSYMediaPlayer_iOS

- Official KSYMediaPlayer License : https://github.com/ksvc/KSYMediaPlayer_iOS/blob/master/LICENSE
