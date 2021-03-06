---
-api-id: M:Windows.Media.Devices.VideoDeviceController.GetMediaStreamProperties(Windows.Media.Capture.MediaStreamType)
-api-type: winrt method
---

<!-- Method syntax
public Windows.Media.MediaProperties.IMediaEncodingProperties GetMediaStreamProperties(Windows.Media.Capture.MediaStreamType mediaStreamType)
-->

# Windows.Media.Devices.VideoDeviceController.GetMediaStreamProperties

## -description
Gets the encoding properties for the specified media stream type for the video device.

## -parameters
### -param mediaStreamType
The type of media stream for which to get the properties.

## -returns
The encoding properties.

## -remarks
The encoding properties returned from this method can either be of type [VideoEncodingProperties](../windows.media.mediaproperties/videoencodingproperties.md) or [ImageEncodingProperties](../windows.media.mediaproperties/imageencodingproperties.md), regardless of the stream type you specify. For this reason, you must check the type of each returned [IMediaEncodingProperties](../windows.media.mediaproperties/imediaencodingproperties.md) object and cast to the appropriate type before accessing the properties of the object. The article [Set media encoding properties for MediaCapture](https://msdn.microsoft.com/en-us/windows/uwp/audio-video-camera/set-media-encoding-properties) provides the complete code for a helper class that handles all necessary type-checking and casting for you.

## -examples

## -see-also
[Set media encoding properties for MediaCapture](https://msdn.microsoft.com/en-us/windows/uwp/audio-video-camera/set-media-encoding-properties), [Camera resolution sample (Windows 10)](http://go.microsoft.com/fwlink/p/?LinkId=624252)