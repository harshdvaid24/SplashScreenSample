# Setup a Splash screen React-Native

Hi! I'm your first Markdown file in **StackEdit**. If you want to learn about StackEdit, you can read me. If you want to play with Markdown, you can edit me. Once you have finished with me, you can create new files by opening the **file explorer** on the left corner of the navigation bar.

# For Android 
## 1. Splash Screen Assets


**Android:**
	First of all the  `mipmap`  folders exist in  `android/app/src/main/res`  and each pixel density has a different density appended to the directory name. Here’s where images should go

-   mipmap-mdpi = icon.png
-   mipmap-hdpi = icon@2x.png
-   mipmap-xhdpi = icon@3x.png
-   mipmap-xxhdpi = icon@3x.png


## 2 create a `background.xml`

First create a `background_splash.xml` file in `android/app/src/main/res/drawable` (you’ll likely have to create the drawable directory).

`<layer-list  xmlns:android="http://schemas.android.com/apk/res/android">`
`<item
android:layout_width="fill_parent"
android:layout_height="wrap_content"
android:drawable="@mipmap/icon"
android:gravity="center"  />`
`</layer-list>`

## 3.  Launch screen implementation

 create a `launch_screen.xml` file in `android/app/src/main/res/layout` (you’ll likely have to create the layout directory).

`<?xml version="1.0" encoding="utf-8"?>`
`<RelativeLayout  xmlns:android="http://schemas.android.com/apk/res/android"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:background="@color/splashscreen_bg"
android:orientation="vertical">`

`<ImageView
android:layout_width="300dp"
android:layout_height="300dp"
android:scaleType="centerInside"
android:layout_centerInParent="true"
android:src="@drawable/background"  />`

`</RelativeLayout>`

## 4. Specify Colors

Next we’ll create a `colors.xml` in `android/app/src/main/res/values` in which we'll define our blue color (which is the same as the blue in our application).

`<color  name="app_bg">#ffffff</color>`
`<color  name="status_bar_color">#ffe43e</color>`
`<color  name="splashscreen_bg">#ffe43e</color>`

## 5. Create a theme for splash screen

Then we create a new `SplashTheme` in the `android/app/src/main/res/values/styles.xml` file.

`<style  name="SplashScreenTheme"  parent="SplashScreen_SplashTheme">`
   `<item  name="colorPrimaryDark">@color/status_bar_color</item>`
`</style>`

## 6. Use React-native-splashscreen

follow steps given in below link **except xml file changes**  b coz We already done above.

-https://www.npmjs.com/package/react-native-splash-screen#installation


## 7. Enjoy your day

# For Ios 
- You can follow  steps of below article.
- https://medium.com/handlebar-labs/how-to-add-a-splash-screen-to-a-react-native-app-ios-and-android-30a3cec835ae

