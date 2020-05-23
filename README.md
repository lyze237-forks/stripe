# Stripe Widgets
A collection of custom Scene2D widgets and utilities for libGDX.

## About

Stripe is a companion to Skin Composer, the renowned UI Skin editor and visual layout utility. This library provides new Scene2D widgets, the capability of loading FreeType fonts from JSON, and the Scene Composer Stage Builder. Please see the wiki for documentation. 

## How to Include in your Project

Typical of most libGDX projects, Stripe requires the Gradle setup to be included your project.

### Core Dependency
Add the following to your root build.gradle:
```groovy
allprojects {
    repositories {
	...
	maven { url 'https://jitpack.io' }
    }
}
```

Add the dependency to your core project:
```groovy
dependencies {
    ...
    compile 'com.ray3k.stripe:stripe:0.0.1-SNAPSHOT'
}
```
If you are using the FreeType Skin Loader, ensure that you have FreeType implemented in your project. Please refer to the libGDX wiki.
### HTML5 Dependency
Add the dependency to your html project of your root build.gradle if you want HTML5/GWT support:
```groovy
project(":html") {
    apply plugin: "gwt"
    apply plugin: "war"

    dependencies {
        ...
        compile 'com.ray3k.stripe:stripe:0.0.1-SNAPSHOT:sources'
    }
}
```

Add the following inherits line to your GdxDefinition.gwt.xml in the html project:
`
<inherits name="com.ray3k.stripe" />
`

If you are using FreeType on HTML5, please follow the instructions to activate gdx-freetype-gwt.

## How to use
Stripe meets a variety of needs, so its implementation is dependent on what utilities you plan to use. Please refer to the wiki:

Stripe Widgets  
FreeType Skin Loader  
Scene Composer Stage Builder
