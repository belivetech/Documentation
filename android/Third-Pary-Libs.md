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
    implementation 'io.grpc:grpc-okhttp:1.26.0'
    implementation 'io.grpc:grpc-protobuf-lite:1.26.0'
    implementation 'io.grpc:grpc-stub:1.26.0'
    implementation 'javax.annotation:javax.annotation-api:1.3.2'

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
    implementation 'com.google.android.exoplayer:exoplayer-ui:2.9.6'

```

## Detailed Explanation 

### Coroutines (Concurrency design pattern for Android)

```
 // coroutines : Use for Aync tasks
    implementation "org.jetbrains.kotlinx:kotlinx-coroutines-android:1.3.6"
    implementation "org.jetbrains.kotlinx:kotlinx-coroutines-core:1.3.6"
```

Official Android developers site : https://developer.android.com/kotlin/coroutines

License : https://github.com/Kotlin/kotlinx.coroutines/blob/master/LICENSE.txt


### KOIN (Dependency Injection)

```
    //dependency injection koin
    api 'org.koin:koin-androidx-scope:2.1.5'
    api 'org.koin:koin-androidx-viewmodel:2.1.5'

```

Official URL : https://insert-koin.io/

Official Github : https://github.com/InsertKoinIO/koin
License : https://github.com/InsertKoinIO/koin/blob/master/LICENSE


### Lifecycle Components

```
    // lifecycle : For lifecycle aware components
    implementation "androidx.lifecycle:lifecycle-extensions:2.2.0-rc02"
    implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:2.2.0-rc02"
    implementation "androidx.lifecycle:lifecycle-livedata-ktx:2.2.0-rc02"
    implementation "androidx.lifecycle:lifecycle-runtime-ktx:2.2.0-rc02"


```

Official Android developers site : https://developer.android.com/jetpack/androidx/releases/lifecycle


### Retrofit (Type safe HTTP client for Android)

```
    // retrofit : Type safe HTTP client for Android
    implementation "com.squareup.retrofit2:retrofit:2.6.1"
    implementation "com.squareup.retrofit2:converter-gson:2.6.1"
    implementation "com.squareup.okhttp3:logging-interceptor:3.10.0"
    implementation 'com.facebook.stetho:stetho-okhttp3:1.5.1'

```

Official Retrofit Github : https://github.com/square/retrofit

Official Retrofit License : https://github.com/square/retrofit/blob/master/LICENSE.txt

Official Okhttp logging intercepter Github (Used only for debug builds) : https://github.com/square/okhttp/tree/master/okhttp-logging-interceptor

Official Okhttp License : https://github.com/square/okhttp/blob/master/LICENSE.txt

Official Stetho site (Use for debugging only): http://facebook.github.io/stetho/

Official Stetho License : https://github.com/facebook/stetho/blob/master/LICENSE

### Realtime-chat 

BeLive has developed in-house chat based on gRPC. We have an alternative option for chat which is developed using Agora RTM SDK. Depending on use case, we can enable and package one of the chat with SDK.

*In-house chat*


```
    //chat : Real time chat depdendencies
    implementation 'io.grpc:grpc-okhttp:1.26.0'
    implementation 'io.grpc:grpc-protobuf-lite:1.26.0'
    implementation 'io.grpc:grpc-stub:1.26.0'
    implementation 'javax.annotation:javax.annotation-api:1.3.2'

```

Official gRPC Github : https://github.com/grpc/grpc-java

Official gRPC License : https://github.com/grpc/grpc-java/blob/master/LICENSE

*Agora Chat*

Official Agora RTM site : https://docs.agora.io/en/Real-time-Messaging/messaging_android?platform=Android
> Note : It's a paid service


### Timber (Debug logs)

```
    //log : For debug logs
    implementation 'com.jakewharton.timber:timber:4.7.1'
```

Official Timber Github : https://github.com/JakeWharton/timber
Official Timber License : https://github.com/JakeWharton/timber/blob/master/LICENSE.txt



### Glide (For Image loading and caching)

```
    // Image loading
    implementation 'com.github.bumptech.glide:glide:4.10.0'
    kapt 'com.github.bumptech.glide:compiler:4.10.0'

```

Official Glide Github :https://github.com/bumptech/glide

Official Glide License : https://github.com/bumptech/glide/blob/master/LICENSE


### Utility libraries for UI 

```
    // misc : Utility libraries for UI 
    implementation 'com.google.code.gson:gson:2.8.6'
    implementation 'androidx.swiperefreshlayout:swiperefreshlayout:1.0.0'
    implementation 'com.hannesdorfmann:adapterdelegates4-kotlin-dsl:4.2.0'

```

Official Gson Github (Used to convert json objects to json representations) : https://github.com/google/gson

Official Gson License :  https://github.com/google/gson/blob/master/LICENSE

Official Swiperefreshlayout (Android official library): https://developer.android.com/jetpack/androidx/releases/swiperefreshlayout

> Note : Swiperefreshlayout is used for Shop catalog UI

Official AdapterDelegates Github :  https://github.com/sockeqwe/AdapterDelegates

Official AdapterDelegates License : https://github.com/sockeqwe/AdapterDelegates/blob/master/LICENSE

> Note : AdapterDelegates is used Chat list UI

### ExoPlayer (Android Media Player)

```
    // exoplayer : Required for playback of streams
    implementation 'com.google.android.exoplayer:exoplayer:2.9.6'
    implementation 'com.google.android.exoplayer:exoplayer-dash:2.9.6'
    implementation 'com.google.android.exoplayer:extension-rtmp:2.9.6'
    implementation 'com.google.android.exoplayer:exoplayer-ui:2.9.6'


```

Official ExoPlayer Github : https://github.com/google/ExoPlayer

Official ExoPlayer License : https://github.com/google/ExoPlayer/blob/release-v2/LICENSE