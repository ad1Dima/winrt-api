---
-api-id: P:Windows.UI.Xaml.Controls.AppBarToggleButton.KeyboardAcceleratorTextOverride
-api-type: winrt property
---

<!-- Property syntax.
public string KeyboardAcceleratorTextOverride { get;  set; }
-->

# Windows.UI.Xaml.Controls.AppBarToggleButton.KeyboardAcceleratorTextOverride

## -description
Gets or sets a string that overrides the default key combination string associated with a [keyboard accelerator](../windows.ui.xaml/uielement_keyboardaccelerators.md).

![Example of a menu showing keyboard accelerators for various menu items](images/keyboard-accelerators.png)  
*Example of a menu showing keyboard accelerators for various menu items*

## -property-value

## -remarks
Windows 10, version 1703, introduced [keyboard accelerator](../windows.ui.xaml/uielement_keyboardaccelerators.md) shortcuts. However, these shortcuts were not displayed with the UI of their corresponding controls.

Starting with Windows 10, version 1803, when [KeyboardAccelerators](../windows.ui.xaml/uielement_keyboardaccelerators.md) are declared, controls display the corresponding key combinations by default.

### Version compatibility

The [KeyboardAcceleratorTextOverride](appbartogglebutton_keyboardacceleratortextoverride.md) property is not available prior to Windows 10, version 1803. If your app’s 'minimum platform version' setting in Microsoft Visual Studio is less than the 'introduced version' shown in the Requirements block later in this page, you must design and test your app to account for this. For more info, see [Version adaptive code](https://msdn.microsoft.com/windows/uwp/debug-test-perf/version-adaptive-code).

To avoid exceptions when your app runs on previous versions of Windows 10, do not set this property in XAML or use it without performing a runtime check. This example shows how to use the [ApiInformation](../windows.foundation.metadata/apiinformation.md) class to check for the presence of this property before you set it.

```xaml
<CommandBar x:Name="commandBar1" Loaded="CommandBar_Loaded">
    <AppBarToggleButton x:Name="appBarButtonShuffle" Icon="Shuffle" Label="Shuffle"/>
</CommandBar>
```

```csharp
private void CommandBar_Loaded(object sender, RoutedEventArgs e)
{
    if (ApiInformation.IsPropertyPresent("Windows.UI.Xaml.Controls.AppBarToggleButton", "KeyboardAcceleratorTextOverride"))
    {
        appBarButtonCut.KeyboardAcceleratorTextOverride = "Ctrl+S";
    }
}
```

## -see-also

## -examples

