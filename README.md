# RaionMobileAnalogInputLibrary
Virtual Game Analog Library for Unity
  
![Generic badge](https://img.shields.io/badge/Version-1.0.1-green.svg)
![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)

## Screenshots
<p align="center">
  <img src="https://raw.githubusercontent.com/jmsrsd/RaionMobileInputAnalog/master/Screenshots/Screenshot.00.gif" height="320"/>
</p>

## Installation
1. Download the \*.unitypackage file(s) in Build dir or in "Build Link" section of this page
2. Open the \*.unitypackage file(s)
3. Click "All" button and then import button in Unity import package dialogue
4. Read "Usage" section of this page to know how to use the library

## Build Link
[.unitypackage](https://github.com/jmsrsd/RaionMobileAnalogInputLibrary/raw/master/Build/101/raion.MobileInputAnalogLibrary.101.unitypackage)  
[.apk](https://github.com/jmsrsd/RaionMobileAnalogInputLibrary/raw/master/Build/apk/100/raion.MobileInputAnalogLibrary.100.apk)
  
## Dir structure
```
Assets
├───raion
│   └───MobileAnalogInput
│       └───Scripts
│           │   Library.cs
│           │
│           └───Internal
│                   Canvas.cs
│                   Helper.cs
│                   UI.cs
│                   UIBackground.cs
│                   UIForeground.cs
│
└───Resources
    └───raion
        └───MobileAnalogInput
            └───Sprites
                    Raion.MobileAnalogInput.Sprite.Circle.png
```
  
## Usage
To initialize the library:
```C#
raion.MobileAnalogInput.Library.GetInstance();
```

To use the library:
```C#
using UnityEngine;

public class LibraryTest : MonoBehaviour {
  private void Update() {
    float speed = 10.0f;

    Vector2 direction =
      raion.MobileAnalogInput.Library.GetInstance().GetDirection();

    Vector3 velocity = Vector3.zero;
    velocity.x = direction.x;
    velocity.z = direction.y;

    // Moving the GameObject
    transform.position += velocity * speed * Time.deltaTime;
  }
}

```
