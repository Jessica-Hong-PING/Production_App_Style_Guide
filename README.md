# Production_App_Style_Guide

HOW TO ADD AND USE THESE STYLES IN YOUR WPF PROJECT:

1. In the Solution Explorer, add a new folder to the main solution called "Styles"
2. Right-click this new folder, select "Add -> Existing Item..." then select the ResourceDictionaries you'd like to include

![populated styles folder](https://github.com/LoganScholz-PING/Production_App_Style_Guide/blob/main/Images/PopulatedStylesFolder.PNG)

3. Inside of App.xaml, you need to merge in these new ResourceDictionaries to the main dictionaries. Add the following code to App.xaml:

![example App.xaml code](https://github.com/LoganScholz-PING/Production_App_Style_Guide/blob/main/Images/AppXamlExample.PNG)

  - NOTE #1: You will always need to register PingColorStyles.xaml first (as in the above example). All other PING custom styles rely on these custom colors
  - NOTE #2: Every ResourceDictionary you include into your project MUST be included on its own line inside App.xaml!

4. To style your control, you need to specify the style in the .xaml. Here is an example of a button with the custom PING style (from MainWindow.xaml):

![button example](https://github.com/LoganScholz-PING/Production_App_Style_Guide/blob/main/Images/ExampleOfButtonWithCustomStyle.PNG)

