# Production_App_Style_Guide
PING Production App Style Guide

HOW TO ADD AND USE THESE STYLES TO YOUR WPF PROJECT:

1. In the Solution Explorer, add a new folder called "Styles":
  - TODO: Picture of empty styles folder
2. Right-click this new folder, select "Add -> Existing Item..." then select the ResourceDictionaries you'd like to include
  - TODO: Picture of populated folder
3. Inside of App.xaml, you need to merge in these new ResourceDictionaries to the main dictionaries. Add the following code to App.xaml:

    <Application.Resources>
        <ResourceDictionary>
            <ResourceDictionary.MergedDictionaries>
                <ResourceDictionary Source="Styles\PingColorStyles.xaml" />
                <ResourceDictionary Source="Styles\PingButtonStyle_Generic.xaml" />
                <ResourceDictionary Source="Styles\[ANOTHER CUSTOM RESOURCE DICTIONARY NAME HERE]" />
                <ResourceDictionary Source="Styles\[ANOTHER CUSTOM RESOURCE DICTIONARY NAME HERE]" />
            </ResourceDictionary.MergedDictionaries>
        </ResourceDictionary>
    </Application.Resources>

  *NOTE #1: Every ResourceDictionary you include into your project MUST be included on its own line inside App.xaml!
  *NOTE #2: You will always need to register PingColorStyles.xaml first (as in the above example). All other PING custom styles rely on these custom colors

4. To style your control, you need to specify the style in the .xaml. Here is an example of a button with the custom PING style (from MainWindow.xaml):

  <Button Style="{StaticResource PingButtonStyle_Generic}" Content="Hello I am a button" Height="200" Width="200" />

5. 
