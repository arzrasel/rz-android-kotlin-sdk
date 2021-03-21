# rz-android-kotlin-sdk
Rz Android Kotlin SDK

[![Rz Rasel](https://raw.githubusercontent.com/arzrasel/svg/main/rz-rasel-blue.svg)](https://github.com/rzrasel)
[![Download](https://api.bintray.com/packages/rzrasel/rz-android-kotlin-sdk/rz-android-kotlin-sdk/images/download.svg) ](https://bintray.com/rzrasel/rz-android-kotlin-sdk/rz-android-kotlin-sdk/_latestVersion)
[![API](https://img.shields.io/badge/API-16%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=16)

### Add Android Dependencies

```android_dependencies
dependencies {
    implementation "com.rzandroid.kotlin:rzandroid-core:0.0.01"
}
```

### Add Maven Repositories (If any problem to implementation)

Add maven repositories in application level (if any problem to implementation then add this code in your gradle file)

```mavenRepositoriesAppProject
allprojects {
    repositories {
        maven { url "https://dl.bintray.com/rzrasel/rz-android-kotlin-sdk" }
    }
}
```

Or add maven repositories in project level

```mavenRepositoriesAppProject
allprojects {
    repositories {
        maven { url "https://dl.bintray.com/rzrasel/rz-android-kotlin-sdk" }
    }
}
```

### Use of Double Click Listener

First option:

Variable declaration

```implementationDoubleClickListener01
private lateinit var button: Button
```
Code implementation
```implementationDoubleClickListener02
val gestureDetector = GestureDetector(context, object : DoubleClickListener() {
    override fun onSingleClick(event: MotionEvent?) {
        // TODO Auto-generated method stub
    }

    override fun onDoubleClick(event: MotionEvent?) {
        // TODO Auto-generated method stub
    }
})
button.setOnTouchListener { view, event -> gestureDetector.onTouchEvent(event); }
```

Second option:

Variable declaration

```implementationDoubleClickListener03
private lateinit var button: Button
```
Code implementation
```implementationDoubleClickListener04
DoubleClickListener.setListener(context, button, object: DoubleClickListener.OnClickListener {
    override fun onSingleClick(event: MotionEvent?) {
        // TODO Auto-generated method stub
    }
    //
    override fun onDoubleClick(event: MotionEvent?) {
        // TODO Auto-generated method stub
    }
})
```
