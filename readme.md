# Floating Action Button

[![Build Status](https://travis-ci.org/shamanland/floating-action-button.svg?branch=demo)](https://travis-ci.org/shamanland/floating-action-button)

A circular button made of paper that lifts and emits ink reactions on press.

This widget supports two sizes according to [Promoted Actions][2] pattern: **normal** and **mini**.

Like an `ImageView` this widget require `android:src` attribute. According to official documentation this drawable should be not more than `24dp`.   

## Gradle dependency

**Release:**

```
repositories {
    mavenCentral()
}

dependencies {
    compile 'com.shamanland:fab:0.0.1'
}
```

**Snapshot:**

```
repositories {
    maven {
        url 'https://oss.sonatype.org/content/groups/public'
    }
}

dependencies {
    compile 'com.shamanland:fab:0.0.1-SNAPSHOT'
}
```

## Screenshots

![light](https://drive.google.com/uc?id=0Bwh0SNLPmjQBRkFoZE04VF90Q2M)
![dark](https://drive.google.com/uc?id=0Bwh0SNLPmjQBZndXMi13Q3l3Qms)

## Customizing

**Use theme to customize all floating buttons in your app:**

Declare own style:

```
<style name="AppTheme.Fab" parent="FloatingActionButton">
    <item name="floatingActionButtonColor">@color/my_fab_color</item>
</style>
```

Link this style in your theme:

```
<style name="AppTheme" parent="android:Theme">
    <item name="floatingActionButtonStyle">@style/AppTheme.Fab</item>
</style>
```

**Customizing in layout.xml:**

```
<com.shamanland.fab.FloatingActionButton
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:src="@drawable/ic_action_my"
    app:floatingActionButtonColor="@color/my_fab_color"
    app:floatingActionButtonSize="mini"
    />
```

**Customizing in java-code:**

```
FloatingActionButton fab = (FloatingActionButton) findViewById(R.id.fab);
fab.setSize(FloatingActionButton.SIZE_MINI);
fab.setColor(Color.RED);
// NOTE invoke this method after setting new values!
fab.initBackground();
// NOTE standard method of ImageView
fab.setImageResource(R.drawable.ic_action_my);
```

## License

```
Copyright 2014 ShamanLand.Com

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

[1]: http://shamanland.github.io/floating-action-button
[2]: http://www.google.com/design/spec/patterns/promoted-actions.html
