1.代码结构和之前的一样，只不过将library-debug_v.x.x.aar包中一部分代码移到app/src/中，提高二次开发简单性。
　开发者不必担心，只需将com.baidu.aip包复制到app/src/main/java中即可。不会影响你的代码结构。

2.如果开发者不想使用gpio,可以将app/libs/中的armeabi-v7a和firefly-api.jar删掉。请将app/build.gradle文件中
     implementation files('libs/firefly-api.jar')注释掉

   并且将AndroidManifest.xml文件中的

     <application
             android:allowBackup="true"
             android:name=".MainApp"
             ...
     中的android:name=".MainApp"去掉。