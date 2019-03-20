# robotDevastation-playground

[Robot Devastation](http://asrob-uc3m.github.io/workgroups/2017-05-28-robot-devastation.html) playground repository.

Experiments that could be later added to robotDevastation. Some of them may be suitable for beginners that want to start developing on robotDevastation :wink:

Originated from https://github.com/asrob-uc3m/robotDevastation/issues/31, this `README.md` should work like an `awesome` list.

* [Hardware](#hardware)
    + [Components](#components)
        - [Brains](#brains)
        - [Solar Panels](#solar-panels)
        - [Worldwide Connectivity](#worldwide-connectivity)
    + [Cool robots that could be supported](#cool-robots-that-could-be-supported)
    + [Cool input devices that could be supported](#cool-input-devices-that-could-be-supported)
* [Software](#software)
    + [Android version](#android-version)
    + [Battery Status](#battery-status)
    + [Augmented Reality (AR)](#augmented-reality-ar)
    + [Bots](#bots)
    + [Cross-compilation](#cross-compilation)
    + [Game Engines](#game-engines)
    + [Monocular SLAM](#monocular-slam)
    + [Plugin Mechanisms](#plugin-mechanisms)
* [Theory](#theory)
    + [Object Persistence](#object-persistence)
* [Our Abandonware](#our-abandonware)

## Hardware

### Components
#### Brains
- ESP8266
- [Raspberry 3 B+](https://www.raspberrypi.org/products/raspberry-pi-3-model-b-plus/): Includes cool wifi spec (2.4GHz and 5GHz IEEE 802.11.b/g/n/ac)!!!
- Orange Pi Lite ([#12](https://github.com/asrob-uc3m/robotDevastation-playground/issues/12))
#### Solar Panels
- We have some!
#### Worldwide Connectivity
- Could be via SIM-card enabled robots (3g/5g...) or by creating a [wireless mesh network](https://en.wikipedia.org/wiki/Wireless_mesh_network) similar to [FireChat](https://en.wikipedia.org/wiki/FireChat).

### Cool robots that could be supported
- [Loki (omnidirectional robot)](https://github.com/davidsanfal/loki)
- [miniKame (cute quadrupted robot)](https://github.com/JavierIH/miniKame)
- [Mizu (quadruped robot)](https://github.com/davidsanfal/mizu)
- [Ganker Robot - Omnidirectional robot with swords](http://gjs.so/en/)

### Cool input devices that could be supported
- XBox controller

## Software

### Android version
*  [Android version of Robot Devastation (just an old idea)](http://wiki.asrob.uc3m.es/index.php/ANDROID)
* Some resources:
    * https://github.com/ZBar/ZBar/tree/master/android
    * https://wiki.libsdl.org/Android
* By having those two and [YARP for Android](https://alecive.github.io/research/2015/08/01/yarpdroid/) to cover all RD dependencies, perhaps the game could be ported to Android with ``nothing more'' than a CMake cross-compile switch. See `BUILD_ANDROID` at https://github.com/robotology/yarp/compare/master...robotology-playground:yarp-android. In case the branch gets deleted: https://github.com/robotology-playground/yarp/commit/fd5eece5d7a378d19b6d78eec45dd97a9e033b00 + https://github.com/robotology-playground/yarp/commit/f47e9996d6e077f8114aa066233c87c047e0f5bb.
* More playground resources:
    * https://www.tensorflow.org/lite
    * https://developers.google.com/ar/discover/

### Augmented Reality (AR)
* https://github.com/robotology/superimpose-mesh-lib
* http://www.slashgear.com/reality-editor-ar-app-connects-iot-devices-by-drawing-lines-15418452/
* http://www.realityeditor.org
* http://www.openhybrid.org/adding-object-and-marker.html

### Battery Status
* Use the YARP [IBattery](http://www.yarp.it/classyarp_1_1dev_1_1IBattery.html) class if we ever get the hardware ([#11](https://github.com/asrob-uc3m/robotDevastation-playground/issues/11) contains mostly broken links).

### Bots
* We could create Non-Playing Characters (NPCs, or simply bots) with Artificial Intelligence (e.g. via Reinforcement Learning). An interesting concept is that of a [Computer game bot Turing Test](https://en.m.wikipedia.org/wiki/Computer_game_bot_Turing_Test), which indicates that Bots with above-human performance can make a game boring.

### Cross-compilation
* https://github.com/dockcross/dockcross

### Game Engines
* [Unity](http://www.unity3d.com/)
* [Unreal](https://www.unrealengine.com/)
* [Ogre](http://www.ogre3d.org/)
* [Irrlicht](http://irrlicht.sourceforge.net/)
* [Crystal Space](http://www.crystalspace3d.org/main/Main_Page)
* [Panda3D](https://github.com/panda3d/panda3d)
* [OpenSceneGraph](http://www.openscenegraph.org)
* [PyGame](https://www.pygame.org)

### Monocular SLAM
* Semi-Direct Monocular Odometry (SVO) [GitHub](https://github.com/uzh-rpg/rpg_svo) [Video](https://www.youtube.com/watch?v=2YnIMfw6bJY)
* Parallel Tracking and Mapping (PTAM) [GitHub](https://github.com/Oxford-PTAM/PTAM-GPL) [Video](https://www.youtube.com/watch?v=Y9HMn6bd-v8)
* A Versatile and Accurate Monocular SLAM (ORB-SLAM) [GitHub](https://github.com/raulmur/ORB_SLAM)
* Real-Time SLAM for Monocular, Stereo and RGB-D Cameras, with Loop Detection and Relocalization Capabilities (ORB-SLAM2) [GitHub](https://github.com/raulmur/ORB_SLAM2)
* ORBSLAM2_with_pointcloud_map [GitHub](https://github.com/gaoxiang12/ORBSLAM2_with_pointcloud_map)
* Large-Scale Direct Monocular SLAM (LSD-SLAM) [GitHub](https://github.com/tum-vision/lsd_slam)

### Plugin Mechanisms
While we mainly use the YARP plugin mechanism for Dynamic Linking plugins, here are some alternatives.
* https://github.com/robotology-playground/sharedlibpp
* Writing DLLs for Linux apps : http://www.ibm.com/developerworks/library/l-dll/
* Stack Overflow (C++: Dynamically loading classes from dlls) : http://stackoverflow.com/questions/431533/c-dynamically-loading-classes-from-dlls
* HowTo: Export classes from a DLL : http://www.codeproject.com/Articles/28969/HowTo-Export-C-classes-from-a-DLL

## Theory

### Object Persistence
* [(Burke, 2001) Creature smarts: The art and architecture of a virtual brain](http://xenia.media.mit.edu/~solan/creatureSmarts.pdf)
* [(Scholl, 2001) Object Persistence in Philosophy and Psychology](http://perception.research.yale.edu/papers/07-Scholl-MindLang.pdf)
* [(Isla, 2002) Object persistence for synthetic creatures](http://www.naimadgames.com/publications/aamas02/aamas02.pdf)
* [(Gkikas, 2007) The evolution of FPS games controllers: how use progressively shaped their present design](http://pci2007.upatras.gr/proceedings/PCI2007_volA/A_037-046_Gkikas.pdf)

## Our Abandonware
* [Trello boards](https://trello.com/robotdevastation) deprecated in favor of our [GitHub project](https://github.com/orgs/asrob-uc3m/projects/1).
* Slack channel `#robotdevastation` on [ASROB workspace](https://asrob.slack.com) deprecated in favor of our [Telegram channel](https://telegram.me/joinchat/ADT1EAjJk_gwAb9GNkqcpA). However, Slack integration with Travis CI could be intersting.
