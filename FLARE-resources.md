# Flare2d
 

 Flutter Flare 1.0 : Getting Started With 2D Animations    
https://youtu.be/eeXdA6gow3s

 
In this video, I will explain how to use flare to create awesome animations. Flare is a product of 2Dimensions. #Flutter #Flare #2DAnimations Please give sta...




# Flare3D


Flare3D is a framework for developing interactive three-dimensional (3D) graphics within Adobe Flash Player and Adobe AIR, written in ActionScript 3.[3] Flare3D includes a 3D object editor (the Flare3D IDE) and a 3D graphics engine for rendering 3D graphics.[1] Flare3D runs on current[when?] web browsers utilizing the Adobe Flash Player, and uses Stage3D for GPU-accelerated rendering. Flare3D has not been under active development since late 2014.[4]

Flare3D has been used to develop popular[vague] browser-based video games such as FarmVille 2 and CityVille 2.[5][6] Flare3D is one of the first frameworks to make GPU-accelerated 3D applications practical for web browsers, and is similar in purpose and design to Away3D.[7][8][9] Flare3D has been used to create 3D models in online applications, such as Space Designer 3D.

The Flare3D platform consists of a 3D world editor, a runtime engine, and a collection of plug-ins for various applications.

The 3D editor may be used to lay out 3D objects, and to generate compressed Flare3D binary packages of 3D models. Such 3D models and animations may be imported from third-party programs such as Autodesk 3ds Max, or Autodesk Maya, or other mesh-based 3D modeller. The 3D runtime engine is typically supplied as a closed-source SWC package, although small portions are released on the GitHub open-source website.[10]

The Flare3D engine uses Stage3D for GPU-accelerated rendering, and contains support for rigid body physics, skeletal animations, and a proprietary GPU-shader language known as FLSL (Flare3D Shader Language).[11] The engine also integrates with FLARToolkit (for augmented reality), Away Physics (from Away3D) and Starling (an Adobe project).[11]

The Flare3D plug-in for Autodesk 3ds Max is provided for free, and enables one-click exporting of a 3D model from 3ds Max to the Flare3D file format.[12] Animation data is also exported, for "Hierarchical" and "Skinned"-based animations.[12] Texture data is automatically converted from unsupported formats to JPG and PNG formats which are supported by the Flare3D engine.[12]

Flare3D has online help and a collaboratively-edited Wiki,[11] forums, tutorials, examples, and documentation.[13]


Rive 1 (previously Flare)
=========================

![](https://cdn.2dimensions.com/flare_macbook.png)

[Rive 1 (previously Flare)](https://www.rive.app/about-flare) offers powerful realtime vector design and animation for app and game designers alike. The primary goal of Flare is to allow designers to work directly with assets that run in their final product, eliminating the need to redo that work in code.

Libraries
---------

There are two Dart packages provided in this repository. [flare\_dart](https://github.com/2d-inc/Flare-Flutter/blob/master/flare_dart) and [flare\_flutter](https://github.com/2d-inc/Flare-Flutter/blob/master/flare_flutter). Most of the time you'll want only [flare\_flutter](https://github.com/2d-inc/Flare-Flutter/blob/master/flare_flutter), especially if you're just starting out with Flare. Please read the details in [flare\_flutter](https://github.com/2d-inc/Flare-Flutter/blob/master/flare_flutter) for how to get your Flare animations running in Flutter!

Flutter Channel
---------------

This repository has three primary branches:

*   stable
    
    *   This is the branch we publish to pub from.
    *   This branch and the associated pub packages are guaranteed to work on the flutter stable channel.
    
        flare_flutter: ^1.8.3
        
    
*   dev
    
    *   This branch has the latest changes should work with the flutter dev channel.
    *   You can point to this branch directly from your pubspec with the following syntax.
    
        flare_flutter:
          git: 
            url: git://github.com/2d-inc/Flare-Flutter.git
            ref: dev
            path: flare_flutter
        
    
*   master
    
    *   This is the branch we work off of for development and the community submits PRs to.
    *   The references in the pubspec here are local, meaning that the intention is to use this library as local reference:
    
        flare_flutter:
          path: ~/my/repos/flare_flutter
        
    

Examples
--------

Take a look at the provided [example applications](https://github.com/2d-inc/Flare-Flutter/tree/master/example).

License
-------

See the [LICENSE](https://github.com/2d-inc/Flare-Flutter/blob/master/LICENSE) file for license rights and limitations (MIT).