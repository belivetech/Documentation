## Third party libraries used by BeLive Android SDK

### Viewer

**Viewer only**

```gradle
// Common libraries for both host and viewer

// coroutines : Use for Aync tasks
implementation "org.jetbrains.kotlinx:kotlinx-coroutines-android:1.3.6"
implementation "org.jetbrains.kotlinx:kotlinx-coroutines-core:1.3.6"

//dependency injection koin
api 'org.koin:koin-androidx-scope:2.1.5'
api 'org.koin:koin-androidx-viewmodel:2.1.5'

// lifecycle : For lifecycle aware components
implementation "androidx.lifecycle:lifecycle-extensions:2.2.0-rc02"
implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:2.2.0-rc02"
implementation "androidx.lifecycle:lifecycle-livedata-ktx:2.2.0-rc02"
implementation "androidx.lifecycle:lifecycle-runtime-ktx:2.2.0-rc02"

// retrofit : Type safe HTTP client for Android
implementation "com.squareup.retrofit2:retrofit:2.6.1"
implementation "com.squareup.retrofit2:converter-gson:2.6.1"
implementation "com.squareup.okhttp3:logging-interceptor:3.10.0"
implementation 'com.facebook.stetho:stetho-okhttp3:1.5.1'

//chat : Real time chat depdendencies
// In-house
implementation 'io.grpc:grpc-okhttp:1.26.0'
implementation 'io.grpc:grpc-protobuf-lite:1.26.0'
implementation 'io.grpc:grpc-stub:1.26.0'
implementation 'javax.annotation:javax.annotation-api:1.3.2'
// Agora
implementation 'com.github.agorabuilder:rtm-sdk:1.4.3'

//log : For debug logs
implementation 'com.jakewharton.timber:timber:4.7.1'

// Image loading
implementation 'com.github.bumptech.glide:glide:4.10.0'
kapt 'com.github.bumptech.glide:compiler:4.10.0'

// misc : Used for developing UI
implementation 'com.google.code.gson:gson:2.8.6'
implementation 'androidx.swiperefreshlayout:swiperefreshlayout:1.0.0'
implementation 'com.hannesdorfmann:adapterdelegates4-kotlin-dsl:4.2.0'

// Viewers only libraries

// exoplayer : Required for playback of streams
implementation 'com.google.android.exoplayer:exoplayer:2.9.6'
implementation 'com.google.android.exoplayer:exoplayer-dash:2.9.6'
implementation 'com.google.android.exoplayer:extension-rtmp:2.9.6'
implementation 'com.google.android.exoplayer:exoplayer-ui:2.9.6'}
```

## Detailed Explanation

### Coroutines

```gradle
// coroutines : Use for Aync tasks
implementation "org.jetbrains.kotlinx:kotlinx-coroutines-android:1.3.6"
implementation "org.jetbrains.kotlinx:kotlinx-coroutines-core:1.3.6"
```

A coroutine is a concurrency design pattern that you can use on Android to simplify code that executes asynchronously. Async tasks are implemented via Kotlin coroutines in BeLive SDK.

- Official Android developers site : https://developer.android.com/kotlin/coroutines
- License : https://github.com/Kotlin/kotlinx.coroutines/blob/master/LICENSE.txt

### KOIN

```gradle
//dependency injection koin
api 'org.koin:koin-androidx-scope:2.1.5'
api 'org.koin:koin-androidx-viewmodel:2.1.5'
```

Koin is a A pragmatic lightweight dependency injection framework for Kotlin developers. Dependency injection is managed via Koin in BeLive SDK.

- Official URL : https://insert-koin.io/
- Official Github : https://github.com/InsertKoinIO/koin
  License : https://github.com/InsertKoinIO/koin/blob/master/LICENSE

### Lifecycle Components

```gradle
// lifecycle : For lifecycle aware components
implementation "androidx.lifecycle:lifecycle-extensions:2.2.0-rc02"
implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:2.2.0-rc02"
implementation "androidx.lifecycle:lifecycle-livedata-ktx:2.2.0-rc02"
implementation "androidx.lifecycle:lifecycle-runtime-ktx:2.2.0-rc02"
```

Lifecycle-aware components perform actions in response to a change in the lifecycle status of another component, such as activities and fragments. BeLive SDK requires Android lifecycle components such as viewmodels and LiveData to implement MVVM architecture.

- Official Android developers site : https://developer.android.com/jetpack/androidx/releases/lifecycle

### Retrofit

```gradle
// retrofit : Type safe HTTP client for Android
implementation "com.squareup.retrofit2:retrofit:2.6.1"
implementation "com.squareup.retrofit2:converter-gson:2.6.1"
implementation "com.squareup.okhttp3:logging-interceptor:3.10.0"
implementation 'com.facebook.stetho:stetho-okhttp3:1.5.1'
```

Retrofit is a type-safe HTTP client for Android and Java. BeLive SDK uses Retrofit to communicate with RESTful APIs of BeLive backend servers.

- Official Retrofit Github : https://github.com/square/retrofit
- Official Retrofit License : https://github.com/square/retrofit/blob/master/LICENSE.txt
- Official Okhttp logging intercepter Github (Used only for debug builds) : https://github.com/square/okhttp/tree/master/okhttp-logging-interceptor
- Official Okhttp License : https://github.com/square/okhttp/blob/master/LICENSE.txt
- Official Stetho site (Use for debugging only): http://facebook.github.io/stetho/
- Official Stetho License : https://github.com/facebook/stetho/blob/master/LICENSE

### Real-time Chat

BeLive has developed in-house chat based on gRPC. We have an alternative option for chat which is developed using Agora RTM SDK. Depending on use case, we can enable and package one of the chat platform with SDK.

_In-house chat_

```gradle
//chat : Real time chat depdendencies
// In-house
implementation 'io.grpc:grpc-okhttp:1.26.0'
implementation 'io.grpc:grpc-protobuf-lite:1.26.0'
implementation 'io.grpc:grpc-stub:1.26.0'
implementation 'javax.annotation:javax.annotation-api:1.3.2'
```

In gRPC, a client application can directly call a method on a server application on a different machine as if it were a local object, making it easier for you to create distributed applications and services. BeLive in-house chat feature is dependent on the gRPC framework.

- Official gRPC Github : https://github.com/grpc/grpc-java
- Official gRPC License : https://github.com/grpc/grpc-java/blob/master/LICENSE

_Agora Chat_

```gradle
// Agora
implementation 'com.github.agorabuilder:rtm-sdk:1.4.3'
```

Agora is a RTM (Real-time Messaging) SDK used to send and receive messages. Agora is required for alternative implementation of real-time chat feature.

- Official Agora RTM site : https://docs.agora.io/en/Real-time-Messaging/messaging_android?platform=Android

> Note : Agora is a paid service.

### Timber

```gradle
//log : For debug logs
implementation 'com.jakewharton.timber:timber:4.7.1'
```

Timber is a logger with a small, extensible API which provides utility on top of Android's normal Log class. Timber is used to debug logs in BeLive SDK.

- Official Timber Github : https://github.com/JakeWharton/timber
- Official Timber License : https://github.com/JakeWharton/timber/blob/master/LICENSE.txt

### Glide

```gradle
// Image loading
implementation 'com.github.bumptech.glide:glide:4.10.0'
kapt 'com.github.bumptech.glide:compiler:4.10.0'
```

Glide is an image loading and caching library for Android focused on smooth scrolling. BeLive SDK requires Glide to process image resources.

- Official Glide Github :https://github.com/bumptech/glide
- Official Glide License : https://github.com/bumptech/glide/blob/master/LICENSE

### Utility libraries for UI

```gradle
// misc : Utility libraries for UI
implementation 'com.google.code.gson:gson:2.8.6'
implementation 'androidx.swiperefreshlayout:swiperefreshlayout:1.0.0'
implementation 'com.hannesdorfmann:adapterdelegates4-kotlin-dsl:4.2.0'
```

Gson is a Java library that can be used to convert Java Objects into their JSON representation. It can also be used to convert a JSON string to an equivalent Java object. BeLive SDK requires Gson to process API responses.

- Official Gson Github: https://github.com/google/gson
- Official Gson License : https://github.com/google/gson/blob/master/LICENSE

Swiperefreshlayout implements the swipe-to-refresh Android UI pattern. It is used for BeLive SDK to implement Shop catalog UI.

- Official Swiperefreshlayout (Android official library): https://developer.android.com/jetpack/androidx/releases/swiperefreshlayout

AdapterDelegates builds your RecyclerView Adapters by composing reusable components. AdapterDelegates is used for BeLive SDK to implement Chat list UI.

- Official AdapterDelegates Github : https://github.com/sockeqwe/AdapterDelegates
- Official AdapterDelegates License : https://github.com/sockeqwe/AdapterDelegates/blob/master/LICENSE

### ExoPlayer

```gradle
// exoplayer : Required for playback of streams
implementation 'com.google.android.exoplayer:exoplayer:2.9.6'
implementation 'com.google.android.exoplayer:exoplayer-dash:2.9.6'
implementation 'com.google.android.exoplayer:extension-rtmp:2.9.6'
implementation 'com.google.android.exoplayer:exoplayer-ui:2.9.6'
```

ExoPlayer is an application level media player for Android developed by Google. BeLive SDK requires ExoPlayer to support playback stream feature.

- Official ExoPlayer Github : https://github.com/google/ExoPlayer
- Official ExoPlayer License : https://github.com/google/ExoPlayer/blob/release-v2/LICENSE
