Vitamin Saber
============

This library provides resource injection for Android (@InjectResource(resId)).
The code is based on the Extra dependency library Dart (https://github.com/f2prateek/dart).

Dependencies
------
```java
class ExampleActivity extends Activity {
  @InjectResource(R.string.hello) String str1;
  @InjectResource(R.color.red) int color;

  @Override public void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.simple_activity);
    VitaminSaber.inject(this);
  }
}
```

Usages
------
```java
class ExampleActivity extends Activity {
  @InjectResource(R.string.hello) String str1;
  @InjectResource(R.color.red) int color;

  @Override public void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.simple_activity);
    VitaminSaber.inject(this);
  }
}
```

Supported Resource Types
-----
```
    anim,
    animator,
    array,
    attr, <- Not supported
    bool,
    color,
    dimen,
    drawable,
    fraction, <- Not supported
    integer,
    interpolator, <- Not supported
    layout,
    menu, <- Not supported
    mipmap, <- Not supported
    plurals, <- Not supported
    raw, <- Not supported
    string,
    style, <- Not supported
    xml
```

Gradle
-----
This project is uploaded to maven central
```
compile "com.w2ji.vitaminsaber:vitaminsaber:1.0.1"
```
-----

Proguard
--------

If Proguard is enabled be sure to add these rules on your configuration:

```
-dontwarn com.w2ji.vitaminsaber.internal.**
-keep class **$$ResourceInjector { *; }
-keepnames class * { @com.w2ji.vitaminsaber.InjectResource *;}
```


License
-------

    Copyright 2015 Wentao Ji

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

