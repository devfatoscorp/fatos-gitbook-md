---
description: How to install FATOS SDK for React-Native
---

# Start

This is a multi-platform map SDK based on React Native. The functions of the SDK are largely composed of map, search, and route planning related operations. The map function can control the map layers, settings, and operation. To use "react-native-fatos-sdk", you must request an SDK key and then apply that key to the source. If you want an SDK key, please go to [https://console.fatos.biz](http://console.fatos.biz/) and request an SDK key after sign up.

Please let us know if you have any technical problems using our SDK   
Contact : [dev@fatoscorp.com](mailto:dev@fatoscorp.com)

{% hint style="info" %}
**If you are a OneMap user, kindly request to** [**https://onemap-console.fatos.biz**](http://onemap-console.fatos.biz/)
{% endhint %}

### Development Environment

#### Install our SDK with npm

```bash
react-native init "project name"
npm i react-native-fatos-sdk
```

In order to use Fatos SDK, you must use your SDK key on your project.  
For Android project, add your key to \[string.xml\] file.  
For iOS project, add your key to \[info.plist\] file.

#### How to run example projects

For you to have a better understanding of our SDK, we included a small example project for Android and iOS. Once you install our SDK, you can run our example projects as follow:

{% tabs %}
{% tab title="Android" %}
1. Go to your Android project folder and navigate to /node\_modules/react-native-fatos-sdk/example
2. Open Android project in example name folder with Android Studio and Press the 'Refactor'\(top of android studio menu\)
3. Select 'Migrate to AndroidX'
4. Migrate the UI library used in the project to AndroidX-based. If build error occurs after migration, AndroidX must be manually applied.

![](https://github.com/devfatoscorp/react-native-fatos-sdk/raw/master/assets/img3.png)
{% endtab %}

{% tab title="iOS" %}
1. Go to your iOS project folder and navigate to /node\_modules/react-native-fatos-sdk/example
2. Run following commands in order

```bash
rm -rf "${HOME}/Library/Caches/CocoaPods"
rm -rf "pwd/Pods/"
pod update
```

    3. Add ResFatos.bundle so that Bundle Resources to be copied

![](https://github.com/devfatoscorp/react-native-fatos-sdk/raw/master/assets/img4.png)
{% endtab %}
{% endtabs %}

Once either of Android or iOS project setting is done, you can run the application with following commands

```bash
react-native run-ios
react-native run-android
```





