# Advance guide for Custom UI

BeLive Android SDK has many ready-to-use features and built-in UI. However, if you want to customize UI based on your specific use case, we provide API for overriding default UI.

## Custom UI for Host Activity 

To add custom layout for host activity, add following method call in `BeliveSdkIntialization.Builder`

```kotlin
 BeliveSdkInitialization.Builder(this)
    .setCustomizedUiForHost(getCustomizedUiForHost())
...

```

We provide **CustomizedXmlUi class** for overiding layouts.

```kotlin
data class CustomizedXmlUi(
    @LayoutRes val xmlPreLiveScreen: Int = 0,
    @LayoutRes val xmlLiveControls: Int = 0,
    @LayoutRes val xmlEndScreen: Int = 0,
    @LayoutRes val xmlPlaybackControls: Int = 0, //for viewer only
    @LayoutRes val xmlCloseButton: Int = 0,
    @LayoutRes val xmlChatInputPopup: Int = 0,
)

```

You can customize following layouts 

- Pre-Live Screen
- Live Stream controls (For example Top and bottom layout)
- End Screen 
- Playback controls - For Viewer only
- Close Button
- Chat Input layout

> You can customize both portrait and landscape views. We support both in our app. For landscape views add them in `layout-land`

We have added some examples in sample app. Use them as starting point to modify UI. You can use custom style and color.

> Note: Use same ID for views. Do not change it. 

```kotlin
 /* Added custom UI option for Host UI */
    private fun getCustomizedUiForHost(): CustomizedXmlUi {
        return CustomizedXmlUi(
            R.layout.layout_host_prelive,
            R.layout.layout_host_live_screen_controllers,
            R.layout.layout_ended_live_host,
            xmlCloseButton = R.layout.view_close_button,
            xmlChatInputPopup = R.layout.layout_chat_input_popup
        )
    }
```

## Custom UI for Viewer Activity 

To add custom layout for viewer activity, add following method call in `BeliveSdkIntialization.Builder`

```kotlin
 BeliveSdkInitialization.Builder(this)
    .setCustomizedUiForViewer(getCustomizedUiForViewer())
...

```
Use example layouts from Sample app as starting point

```kotlin
    /* Added custom UI option for Viewer UI */
    private fun getCustomizedUiForViewer(): CustomizedXmlUi {
        return CustomizedXmlUi(
            R.layout.layout_viewer_prelive,
            R.layout.layout_live_viewer_screen_controllers,
            R.layout.layout_viewer_live_ended,
            xmlCloseButton = R.layout.view_close_button,
            xmlChatInputPopup = R.layout.layout_chat_input_popup
        )
    }
```

> In case you don't want to override certain layout, set value as `0`

## Custom UI for Chat layout

To add custom layout for chat layout, add following method call in `BeliveSdkIntialization.Builder`

```kotlin
 BeliveSdkInitialization.Builder(this)
    .setCustomizedChatMessageStyle(getCustomizedChatMessageStyle())
...

```
You can modify following parameters in chat layout 

```kotlin
data class ChatMessageStyles(
    val textSize: Int,
    @DrawableRes val backgroundColor: Int,
    val displayNameColor: String,
    val textMessageColor: String,
    @FontRes val displayNameFont: Int,
    @FontRes val textMessageFont: Int
)
```

Refer to following example.

```kotlin
    /* Added custom style for chat message */
    private fun getCustomizedChatMessageStyle(): ChatMessageStyles? {
        return ChatMessageStyles(
                12, R.drawable.bg_chat_message_customized,
                "#eda461", "#1de5c0",
                R.font.roboto_medium, R.font.roboto_regular)
    }
```