#QtKnobs
QtKnobs is a Qt and QML based Library/Plugin which provides different types of Knobs.

Screenshots:
- ###### Types

  ![ScreenShot](https://raw.githubusercontent.com/ashish157/Knobs-n-Dials-QML/5c5e347b649606533a95330b9cafb3b4eb4b8155/QtKnobs/screens/alltypes.png)

- ###### Percent View

  ![ScreenShot](https://raw.githubusercontent.com/ashish157/Knobs-n-Dials-QML/5c5e347b649606533a95330b9cafb3b4eb4b8155/QtKnobs/screens/percent.png)

- ###### Minimum & Maximum values

  ![ScreenShot](https://raw.githubusercontent.com/ashish157/QtKnobs/master/QtKnobs/screens/minandmax.png)
  
- ###### Various Sizes

  ![ScreenShot](https://raw.githubusercontent.com/ashish157/Knobs-n-Dials-QML/5c5e347b649606533a95330b9cafb3b4eb4b8155/QtKnobs/screens/sizes.png)
  
- ###### Customize

  ![ScreenShot](https://raw.githubusercontent.com/ashish157/Knobs-n-Dials-QML/5c5e347b649606533a95330b9cafb3b4eb4b8155/QtKnobs/screens/custom.png)

#List of properties
* size
* value
* minimumValue
* maximumValue
* percent
* readOnly { true, false }
* mode { Knob.Normal, Knob.Percent }
* style { Knob.Pie, Knob.Arc, Knob.Needle }
* pieType { Knob.Flat, Knob.Curve  } (**when style = Knob.Pie**)
* needleType { Knob.Point, Knob.Round, Knob.Groove  } (**when style = Knob.Needle**)
* color (**knob color**)
* backgroundColor (**back dial color**)
* foregroundColor (**front dial color**)
* borderColor
* textColor
* meter { true, false } (**simple meter**)
* pieMultiColor (some fun)
 
#Requirement
Qt >= 5.3

#Building
* Clone
* Run qmake && make && make install

The compiled plugin (libqtknobsplugin.so on .nix systems) would be in directory **imports/QtKnobs** with file **qmldir**.

#Use
If you **make install** then you need not do anything. But just in case if you want it to be included in your application then: 
* Copy directory **imports** to your project location  
* To make the engine to search for this module, add the path where the **imports** directory is using *addImportPath*.  
For eg. If the directory **imports** is at location */home/ashish/KnobsTest* then,
```
QQuickView view;
view.engine()->addImportPath("/home/ashish/KnobsTest/imports");
view.show();
```
* Additionally, to make QtCreator aware of it (and to get rid of the annoying **QML module not found** during import) add the path in .pro file,
```
QML_IMPORT_PATH = /home/ashish/KnobsTest/imports
```

#Examples

* A simple Knob:
  
  ```
  import QtQuick 2.0
  import QtKnobs 1.0
  Knob {
    value: 25
  }
  ```

  ![ScreenShot](https://raw.githubusercontent.com/ashish157/Knobs-n-Dials-QML/5c5e347b649606533a95330b9cafb3b4eb4b8155/QtKnobs/screens/default.png)

   You can find more examples in QtKnobs/examples/main.qml

#License

MIT

#Contact
Feel free to contact me for any questions at ashishd157 at gmail.com.
