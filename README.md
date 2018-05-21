<br/>
<p align="center">
  <a href="http://devlight.io">
      <img src ="https://drive.google.com/uc?export=download&id=0BxPO_UeS7wScLVBKck51Z1Rzb0E" alt="Devlight"/>
  </a>
</p>
<br/>

ArcProgressStackView
====================

Present your progress bars in arc mode with information and total control.

[![Android Arsenal](https://drive.google.com/uc?export=download&id=0BxPO_UeS7wScVWk2RmJHNGJGWUk)](http://android-arsenal.com/details/1/3308)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[![Android](https://drive.google.com/uc?export=download&id=0BxPO_UeS7wSccEZaclNGN0R5OWc)](https://github.com/DevLight-Mobile-Agency)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[![Download](https://drive.google.com/uc?export=download&id=0BxPO_UeS7wScaDl2U0QtWUx3emM)](https://bintray.com/gigamole/maven/apsv/_latestVersion)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[![License](https://drive.google.com/uc?export=download&id=0BxPO_UeS7wScU0tmeFpGMHVWNWs)](https://github.com/DevLight-Mobile-Agency/ArcProgressStackView/blob/master/LICENSE.txt)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[![Codacy](https://drive.google.com/uc?export=download&id=0BxPO_UeS7wScSHhmckZyeGJDcXc)](https://www.codacy.com/app/gigamole53/ArcProgressStackView?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=DevLight-Mobile-Agency/ArcProgressStackView&amp;utm_campaign=Badge_Grade)

<p align="center">
    <img src="https://drive.google.com/uc?export=download&id=0BxPO_UeS7wScTjlVNklhUHZibVE"/>
</p>

You can check the sample app [here](https://github.com/DevLight-Mobile-Agency/ArcProgressStackView/tree/master/app).

Warn
====
```
This library is not more supported. 
If you want to add new feature or fix a bug, grab source code and do it. 
If you think your fix or feature would be useful to other developers, 
I can add link of your repository to this README file. 
Thank you for using our libraries.
```

Download
========

You can download a `.aar` from GitHub's [releases page](https://github.com/DevLight-Mobile-Agency/ArcProgressStackView/releases).

Or use Gradle:

```groovy
implementation 'devlight.io:arcprogressstackview:1.0.4'
```

Or Maven:  
```xml
<dependency>
  <groupId>devlight.io</groupId>
  <artifactId>arcprogressstackview</artifactId>
  <version>1.0.4</version>
  <type>pom</type>
</dependency>
```

Or Ivy:  
```groovy
<dependency org='devlight.io' name='arcprogressstackview' rev='1.0.4'>
  <artifact name='$AID' ext='pom'></artifact>
</dependency>
```


Android SDK Version
===================

`ArcProgressStackView` requires a minimum SDK version of 8, but if you want animation and shadow support it requires a minimum SDK version of 11.

Sample
======

<b>Parameters</b>

For `APSV` you can set such parameters as:

 - models:  
    allows you to set `APSV` models, where you set title, progress and colors. Can be set up only via code.

 - animation:  
    allows you to animate progress with func call or with touch event.

 - shadow:  
    allows you to add shadow to your progress models, but remember, the shadow need `LAYER_TYPE_SOFTWARE`, so it decrease FPS.

 - round corners:  
    allows you to set round corners to models.

 - drag/seek:  
    allows you to make your progress model seek like.

 - typeface:  
    allows you to set custom typeface.

 - text color:  
    allows you to set text(title and progress indicator) color.

 - shadow distance:  
    allows you to set shadow distance.

 - shadow angle:  
    allows you to set shadow angle.

 - shadow radius:  
     allows you to set shadow radius.

 - shadow color:  
     allows you to set shadow color.

 - animation duration:  
     allows you to set animation duration.

 - animation listener:  
     allows you to set animation listener.

 - interpolator:  
     allows you to set interpolator to animation.

 - draw width:  
     allows you to set draw width in fraction mode(e.g. 55%) or dimension mode.

 - model offset:  
     allows you to set model offset(positive or negative).

 - model background:  
     allows you to set model background track from start angle to sweep angle.

 - start angle:  
     allows you to set start angle of models.

 - sweep angle:  
     allows you to set sweep angle of models.

 - progress indicator orientation:  
     allows you to set progress indicator orientation.

 - preview colors:  
     allows you to set preview colors, which generate count of models equals to count of colors.

 - preview background:  
    allows you to set models background preview color.

<b>Tips</b>

All angle variables can only be positive and be in range from 0 to 360 degrees.  
The size of `View` automatically set up in square mode.

<b>Init</b>

Check out in code init:

```java
final ArrayList<ArcProgressStackView.Model> models = new ArrayList<>();
models.add(new ArcProgressStackView.Model("Circle", 25, bgColors[0], mStartColors[0]));
models.add(new ArcProgressStackView.Model("Progress", 50, bgColors[1], mStartColors[1]));
models.add(new ArcProgressStackView.Model("Stack", 75, bgColors[2], mStartColors[2]));
models.add(new ArcProgressStackView.Model("View", 100, bgColors[3], mStartColors[3]));

final ArcProgressStackView arcProgressStackView = (ArcProgressStackView) findViewById(R.id.apsv);
arcProgressStackView.setModels(models);
```

Other methods check out in sample.

And `XML` init:

```xml
<devlight.io.library.ArcProgressStackView
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    app:apsv_rounded="true"
    app:apsv_shadowed="true"
    app:apsv_animated="true"
    app:apsv_dragged="true"
    app:apsv_leveled="true"
    app:apsv_typeface="fonts/agency.ttf"
    app:apsv_text_color="#fff"
    app:apsv_shadow_distance="5dp"
    app:apsv_shadow_angle="90"
    app:apsv_shadow_radius="10dp"
    app:apsv_shadow_color="#000"
    app:apsv_animation_duration="1000"
    app:apsv_interpolator="@android:anim/bounce_interpolator"
    app:apsv_draw_width="75%"
    app:apsv_model_offset="5dp"
    app:apsv_model_bg_enabled="true"
    app:apsv_start_angle="270"
    app:apsv_sweep_angle="360"
    app:apsv_indicator_orientation="vertical"
    app:apsv_preview_colors="@array/default_preview"
    app:apsv_preview_bg="#ccc"/>
```

Getting Help
============

To report a specific problem or feature request, [open a new issue on Github](https://github.com/DevLight-Mobile-Agency/ArcProgressStackView/issues/new).

Credits
=======

|[Ron Evgeniy](https://www.behance.net/RonEvgeniy)|[Virgil Pana](https://dribbble.com/virgilpana)|[Gleb Kuznetsov](https://dribbble.com/glebich)|
|:-----------------------------------------------:|:--------------------------------------------:|:--------------------------------------------:|
|[![](https://drive.google.com/uc?export=download&id=0BxPO_UeS7wScQm9QbjV4VWh2R2c)](https://www.behance.net/gallery/33128783/12-weeks-marathon-in-Sketch)|[![](https://drive.google.com/uc?export=download&id=0BxPO_UeS7wScc1Qyd0pMQm5vd0U)](https://dribbble.com/shots/1926158-Data-Visualization)|[![](https://drive.google.com/uc?export=download&id=0BxPO_UeS7wScakVhdXpENlJQdXc)](https://dribbble.com/shots/2123768-graph-ios-app)|

Author
======

Created by [Basil Miller](https://github.com/GIGAMOLE) - [@gigamole](mailto:gigamole53@gmail.com)

Company
=======

[![Facebook](https://drive.google.com/uc?export=download&id=0BxPO_UeS7wScaGhGVFNKU0VxMnc)](https://www.facebook.com/devlightagency)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[![Twitter](https://drive.google.com/uc?export=download&id=0BxPO_UeS7wScZ1ExQWh5cHF5cVE)](https://twitter.com/DevLightIO)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[![LinkedIn](https://drive.google.com/uc?export=download&id=0BxPO_UeS7wSccGZINzEycE1nVFE)](https://www.linkedin.com/company/devlight)


Created by [Basil Miller](https://github.com/GIGAMOLE) - [@gigamole](mailto:gigamole53@gmail.com)
=======
[Here](https://github.com/DevLight) you can see open source work developed by Devlight LLC.  
This and another works is an exclusive property of Devlight LLC. 

If you want to use this library in applications which will be available on Google Play, please report us or author of the library about it.

Whether you're searching for a new partner or trusted team for creating your new great product we are always ready to start work with you. 

You can contact us: info@devlight.io or opensource@devlight.io.  
Thanks in advance.

Devlight LLC, 2016  
[devlight.io](http://devlight.io)
