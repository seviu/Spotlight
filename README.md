# Spotlight
Spotlight is an Android library used to onboard users by showcasing specific features in the app.

[![Platform](https://img.shields.io/badge/platform-android-green.svg)](http://developer.android.com/index.html)
<img src="https://img.shields.io/badge/license-Apache 2.0-green.svg?style=flat">
[![API](https://img.shields.io/badge/API-11%2B-green.svg?style=flat)](https://android-arsenal.com/api?level=11)
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-Spotlight-green.svg?style=flat)](http://android-arsenal.com/details/1/3730)

#Screen
![Sample](https://github.com/PGrube26/Spotlight/blob/master/art/sample.gif)

#Usage
```java
new SpotlightView.Builder(this)
                .introAnimationDuration(400)
                .enableRevealAnimation(isRevealEnabled)
                .performClick(true)
                .maskColor(Color.parseColor("#dc000000"))
                .target(view)
                .lineAnimationDuration(200)
                .setDescriptionView(R.layout.sample_description_view)
                .lineAndArcColor(Color.parseColor("#e1e1e1"))
                .dismissOnTouch(true)
                .enableDismissAfterShown(true)
                .showCircle(SPOTLIGHT_ID);
```

## Download
### Gradle

1. Add it in your root `build.gradle` at the end of repositories:

    ```javascript
    allprojects {
    	repositories {
    		...
    		maven { url "https://jitpack.io" }
    	}
    }
    ```

2. Add the dependency

    ```javascript
    dependencies {
        compile 'com.github.PGrube26:Spotlight:1.0.0'
    }
    ```

### Maven

1. Add it in your `pom.xml` at the end of repositories:

    ```xml
    <repositories>
        ...
    	<repository>
    	    <id>jitpack.io</id>
    	    <url>https://jitpack.io</url>
    	</repository>
    </repositories>
    ```

2. Add the dependency

    ```xml
    <dependency>
        <groupId>com.github.PGrube26</groupId>
        <artifactId>Spotlight</artifactId>
        <version>1.0.0</version>
    </dependency>
    ```

# Configuration Method
```java
//Create global config instance to reuse it
SpotlightConfig config = new SpotlightConfig();
config.isDismissOnTouch(true);
config.setLineAndArcColor(0xFFFFFFFF);
...
.setConfiguration(config) //
```

#Proguard rules

```java
-keep class com.wooplr.spotlight.** { *; }
-keep interface com.wooplr.spotlight.**
-keep enum com.wooplr.spotlight.**
```

#Credits
[Jitender Chaudhary](https://github.com/29jitender)

[MaterialIntroView](https://github.com/iammert/MaterialIntroView)

[Rahul Khanna](https://www.linkedin.com/in/rahul-khanna-01705827)

[Suraj Barthy](https://dribbble.com/thesbdesign)

## License
[Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0.txt)
