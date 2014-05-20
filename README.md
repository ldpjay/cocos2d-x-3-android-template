##Easy Run cocos2d-x-3.x in Eclipse 

Cocos2d-x Official's Android project template is incorrect. so,I fix it, You can easy run cocos2d-x-3.x in eclipse by two steps !!!

At first, you should download this template and replace the incorrect template at `cocos2d-x-3.0/templates/cpp-template-default`

You also can use it for lua/js projects by a little change.

### Prerequisites:

* Android NDK
* Android SDK **OR** Eclipse ADT Bundle
* Android AVD target installed
* Command line Building project successed

You can read official [README.md](https://github.com/cocos2d/cocos2d-x/blob/v3/README.md) to finish it

####Step 1: C/C++ Environment Variable `NDK_ROOT`

* Eclipse->Preferences->C/C++->Build->**Environment**.
* Click **Add** button and add a new variable `NDK_ROOT` pointing to the root NDK directory.
	![Example](https://lh3.googleusercontent.com/-AVcY8IAT0_g/UUOYltoRobI/AAAAAAAAsdM/22D2J9u3sig/s400/cocos2d-x-eclipse-ndk.png)
	

####Step 2: Adding and running from Eclipse

![Example](https://lh3.googleusercontent.com/-SLBOu6e3QbE/UUOcOXYaGqI/AAAAAAAAsdo/tYBY2SylOSM/s288/cocos2d-x-eclipse-project-from-code.png) 

![Import](https://lh5.googleusercontent.com/-XzC9Pn65USc/UUOcOTAwizI/AAAAAAAAsdk/4b6YM-oim9Y/s400/cocos2d-x-eclipse-import-project.png)

1. File->New->Project->Android Project From Existing Code
2. **Browse** to your project directory and Add the project 
3. Click **Run as Android Application** to run on connected device or emulator.

That's all !!! 

###Ant Build

You need download ant at first,also confim you have install correct android sdk version where target set in `project.properties`.

    1. ./proj.android/project.properties  target
    2. ./cocos2d/cocos2d/cocos/2d/platform/android/java/project.properties target

`ant -file build.xml -Dsdk.dir=/Your/Android/sdk/path clean debug`

### Features:

1. No errors on Editor
   
    `closed eclipse Code Analysis's error option`
 
2. Perfect Indexer!

    `Add two symbols at Eclipse's c++ General settings`
   
3. Auto find cpp files

    `Android.mk can auto find cpp files from Classes and jni directory.`

4. Add libcocos2d as a link directory
    
    `you need not to add libcocos2d any more.`
    
### To do List

1. Android Proguard support
2. NDK debug support

You can fork this template at [My Github](https://github.com/myourys/cocos2d-x-3-android-template).
	
