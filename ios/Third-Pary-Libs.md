## Third party libraries used by BeLive iOS SDK

### Viewer 

**Viewer only**

> Live stream libraries are not required if HLS playback is preferred. It is omitted from this document

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

```
   #MARK: - Network
    pod 'Alamofire', '4.9.1'
    pod 'AlamofireObjectMapper', '5.2.1'
    pod 'SDWebImage', '5.11.0'
     

```

Official Alamofire Github : https://github.com/Alamofire/Alamofire

Official Alamofire License : https://github.com/Alamofire/Alamofire/blob/master/LICENSE

Official AlamofireObjectMapper Github : https://github.com/tristanhimmelman/AlamofireObjectMapper

Official AlamofireObjectMapper License : https://github.com/tristanhimmelman/AlamofireObjectMapper/blob/master/LICENSE

Official SDWebImage Github : https://github.com/SDWebImage/SDWebImage

Official SDWebImage License : https://github.com/SDWebImage/SDWebImage/blob/master/LICENSE


### Real-time chat

BeLive has developed in-house chat based on gRPC. We have an alternative option for chat which is developed using Agora RTM SDK. Depending on use case, we can enable and package one of the chat platform with SDK.

```
    #MARK: - Chat - in-House (gRPC)
    pod 'SwiftGRPC', '0.11.0'
    pod 'gRPC', '1.24.2'
    pod 'pop', '1.0.12'
```

*In-house chat*

Official gRPC Github : https://github.com/grpc/grpc-swift

Official gRPC License : https://github.com/grpc/grpc-swift/blob/main/LICENSE

*Agora Chat*

```
    #MARK: - Chat - Agora RTM
    pod 'AgoraRtm_iOS', '1.4.3'


```

Official Agora RTM site : https://docs.agora.io/en/Real-time-Messaging/messaging_ios?platform=iOS
> Note : It's a paid service



### Utility Libraries for iOS

```
    #MARK: - Util - For UI
    pod 'ObjectMapper', '3.5.3'
    pod 'PromiseKit', '6.13.1'
    pod 'IQKeyboardManagerSwift', '6.5.6'
    pod 'Toast-Swift', '5.0.1'
    pod 'SnapKit', '5.0.1'
    pod 'SVProgressHUD', '2.2.5'
    pod 'SwiftyPlistManager', '1.0.2'


```

Official ObjectMapper Github (Converting model to and from JSON) : https://github.com/tristanhimmelman/ObjectMapper

Official ObjectMapper License : https://github.com/tristanhimmelman/ObjectMapper/blob/master/LICENSE

Official PromiseKit Github (Use for asynchronous tasks) : https://github.com/mxcl/PromiseKit

Official PromiseKit License : https://github.com/mxcl/PromiseKit/blob/master/LICENSE

Official IQKeyboardManagerSwift Github (For handling of keyboard in chat UI) : https://github.com/hackiftekhar/IQKeyboardManager

Official IQKeyboardManagerSwift License : https://github.com/hackiftekhar/IQKeyboardManager/blob/master/LICENSE.md

Official Toast-Swift Github (Used for toast notification in UIView class) : https://github.com/scalessec/Toast-Swift

Official Toast-Swift License : https://github.com/scalessec/Toast-Swift/blob/master/LICENSE

Official SnapKit Github (Utility library for auto-layout) : https://github.com/SnapKit/SnapKit

Official SnapKit License : https://github.com/SnapKit/SnapKit/blob/develop/LICENSE

Official SVProgressHUD Gitbub (Utility UI library for displaying progress) : https://github.com/SVProgressHUD/SVProgressHUD

Official SVProgressHUD License : https://github.com/SVProgressHUD/SVProgressHUD/blob/master/LICENSE

Official SwiftyPlistManager Github (Used for plist data management to manage SDK configurations) : https://github.com/rebeloper/SwiftyPlistManager

Official SwiftyPlistManager License : https://github.com/rebeloper/SwiftyPlistManager/blob/master/LICENSE

### Reactive Extensions (Rx)

```
    #MARK: - Reactive extensions - Rx
    pod 'RxSwift', '5.1.2'
    pod 'RxCocoa', '5.1.1'
    pod 'RxRelay', '5.1.1'
    pod 'RxAppState', '1.6.0'
    pod 'RxReachability', '1.1.0'

```

Official Rx Github (Use for asynchronous programming): https://github.com/ReactiveX/RxSwift

Official Rx License : https://github.com/ReactiveX/RxSwift/blob/main/LICENSE.md

### License (CryptoSwift)

```
    #MARK: - License - CryptoSwift
    pod 'CryptoSwift', '1.3.8'

```

Official CryptoSwift Github (Use for license verificaiton of SDK) : https://github.com/krzyzanowskim/CryptoSwift

Official CryptoSwift License : https://github.com/krzyzanowskim/CryptoSwift/blob/master/LICENSE

### Appendix 

In case of `non-HLS playback such as RTMP, FLV etc.`, We use KSYMediaPlayer 

Official KSYMediaPlayer Github : https://github.com/ksvc/KSYMediaPlayer_iOS

Official KSYMediaPlayer License : https://github.com/ksvc/KSYMediaPlayer_iOS/blob/master/LICENSE


