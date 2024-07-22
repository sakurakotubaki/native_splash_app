# native_splash_app

A new Flutter project.

## Getting Started

[zenn](https://zenn.dev/jboy_blog/articles/c794bf8efd39cd)

[official](https://pub.dev/packages/flutter_native_splash)

add package:
```shell
flutter pub add flutter_native_splash
```

create 📁assets
```shell
mkdir assets
```

create image:
```shell
flutter pub pub run flutter_native_splash:create
```

remove image:
```shell
flutter pub run flutter_native_splash:remove
```

## androidだけ表示されない?
android12以降は、アイコンをスプラッシュとするようになったので、設定が必要。

[android developer](https://developer.android.com/develop/ui/views/launch/splash-screen/migrate?hl=ja&_gl=1*l6qvvo*_up*MQ..*_ga*NTcxMDE4NjMxLjE3MjE2MTEzNDI.*_ga_6HH9YJMN9M*MTcyMTYxMTM0Mi4xLjAuMTcyMTYxMTM0Mi4wLjAuMA..)
[official](https://pub.dev/packages/flutter_launcher_icons)

add: package:
```shell
flutter pub add flutter_launcher_icons
```

android sdkの設定を追加
```
defaultConfig {
        // TODO: Specify your own unique Application ID (https://developer.android.com/studio/build/application-id.html).
        applicationId = "com.jboycode.native_splash_app"
        // You can update the following values to match your application needs.
        // For more information, see: https://docs.flutter.dev/deployment/android#reviewing-the-gradle-build-configuration.
        minSdk = 23
        targetSdk = 34
        versionCode = flutterVersionCode.toInteger()
        versionName = flutterVersionName
    }
```

crete icon:
```shell
flutter pub run flutter_launcher_icons:main
```