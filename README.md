[![Android Arsenal]( https://img.shields.io/badge/Android%20Arsenal-SharedPrefManager-green.svg?style=flat )]( https://android-arsenal.com/details/1/7047 )


# SharedPref Manager

**get sample apk from [Google Play Store][googlePlayStoreLink]**

<img src="https://raw.githubusercontent.com/Ashok-Varma/SharedPrefManager/master/sharedpref_320_5_compressed.gif" width="300" height="550" />

## What is this library about?
SharedPref Manager helps to manage your android Shared Preferences very effectively with ease

**(currently under active development, expect to see new releases almost daily)**

## Features

* Edit a SharedPreferences Item
* Add a SharedPreference Item
* Clear All SharedPreferences
* Delete a SharedPreference Item

## Download

Based on your IDE you can import library in one of the following ways

Gradle:
```groovy
debugCompile 'com.ashokvarma.android:sharedpref-manager:1.0.5'
releaseCompile 'com.ashokvarma.android:sharedpref-manager-no-op:1.0.5'
```
If you want this in library in production also then try this : 
```groovy
compile 'com.ashokvarma.android:sharedpref-manager:1.0.5'
```


or grab via Maven:
```xml
<dependency>
  <groupId>com.ashokvarma.android</groupId>
  <artifactId>sharedpref-manager</artifactId>
  <version>1.0.5</version>
  <type>pom</type>
</dependency>
```

or Ivy:
```xml
<dependency org='com.ashokvarma.android' name='sharedpref-manager' rev='1.0.5'>
  <artifact name='$AID' ext='pom'></artifact>
</dependency>
```

or Download [the latest JAR][mavenAarDownload]


## Usage

All the Shared-Pref Names to be should be sent to SharedPrefManager. It does remaining heavy lifting.
#### Sample Code
```java
SharedPrefManager
        .launchSharedPrefManager(
                context
                , new ArrayList<>(Arrays.asList(new String[]{"SHARED_PREF_1_PRIVATE", "SHARED_PREF_2_PRIVATE"}))// All your MODE_PRIVATE shared Shared Preference names, Null if None
                , new ArrayList<>(Arrays.asList(new String[]{"SP_WORLD_READ"}))//All your MODE_WORLD_READABLE Shared Preference Names, Null if None
                , new ArrayList<>(Arrays.asList(new String[]{"SP_WORLD_WRITE"}))//All your MODE_WORLD_READABLE Shared Preference Names, Null if None
         );
```
MODE_WORLD_READABLE, MODE_WORLD_READABLE are not supported by android system in Android N(Nougat) and above devices, If sent those will be ignored in Android N and above devices.

## License

```
SharedPref Manager library for Android
Copyright (c) 2016 Ashok Varma (http://ashokvarma.me/).

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

## Other Open Source Libraries
1. [Gander](https://github.com/Ashok-Varma/Gander) : Gander is a simple in-app HTTP inspector for Android OkHttp clients. Gander intercepts and persists all HTTP requests and responses inside your application, and provides a UI for inspecting their content.
2. [SqliteManager](https://github.com/Ashok-Varma/SqliteManager) : Sqlite Manager is a Dev Debug tool that helps to manage(Edit, Add, Clear) your android Sqlite Databases.
3. [BottomNavigation](https://github.com/Ashok-Varma/BottomNavigation) : This Library helps users to use Bottom Navigation Bar (A new pattern from google) with ease and allows ton of customizations.

[mavenAarDownload]: https://repo1.maven.org/maven2/com/ashokvarma/android/sharedpref-manager/1.0.5/sharedpref-manager-1.0.5.aar
[googlePlayStoreLink]: https://play.google.com/store/apps/details?id=com.ashokvarma.sharedprefmanager.sample
