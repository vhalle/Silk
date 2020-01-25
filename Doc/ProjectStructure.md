# Project Structure Guideline

- [Scene Structure](##-Scene-Structure)
- [Assets Structure](##-Assets-Structure)
- [Additional Resources](##-Additional-Resources)

## Scene Structure

Use empty gameobjects to structure the scene hierarchy.

```
|-- Management
|-- GUI
|-- Cameras
|-- Lights
|-- World
    |-- Terrain
    |-- Props
|-- _Dynamic
```

1. All empty objects should be located at 0,0,0 with default rotation and scale.
1. When you’re instantiating an object in runtime, make sure to put it in _Dynamic – do not pollute the root of your hierarchy or you will find it difficult to navigate through it.
1. For empty objects that are only containers for scripts, use “@” as prefix – e.g. @Cheats

## Assets Structure

```
|-- Assets
    |-- Animations
        |-- 2DAnimations
        |-- 3DAnimations
    |-- Media
        |-- Audio
            |-- Music
            |-- SFX
        |-- Video
    |-- Materials
    |-- Models
    |-- Plugins             //Special Folder
    |-- Prefabs
    |-- Textures
    |-- Scenes
        |-- Levels
        |-- Others
    |-- Scripts
        |-- Editor          //Special Folder
    |-- Shaders    
    |-- Standard Assets     //Special Folder
    |-- StreamingAssets     //Special Folder
    |-- Sprites
```

1. Do not store any asset files in the root directory. Use subdirectories whenever possible.
1. Do not create any additional directories in the root directory, unless you really need to.
1. Be consistent with naming.
1. Don’t try to move context-specific assets to the general directories. 
    - For instance, if there are materials generated from the model, don’t move them to Materials directory because later you won’t know where these come from.
1. Leave 3rd-Party assets imported from the Asset Store in `Standard Assets`. They usually have their own structure that shouldn’t be altered.

### Unity Special Folder

> You can usually choose any name you like for the folders you create to organise your Unity project. However, there are a number of folder names that Unity interprets as an instruction that the folder’s contents should be treated in a special way.

[Official Documentation](https://docs.unity3d.com/Manual/SpecialFolders.html)

> Some of these folders have an effect on the order of script compilation.

[Special folders and script compilation order](https://docs.unity3d.com/Manual/ScriptCompileOrderFolders.html)

#### Regular Folders

- `Assets/*/Editor`
- `Assets/*/Resources`

#### Unique Folders

- `Assets/Editor Default Resources`
- `Assets/Gizmos`
- `Assets/Standard Assets`
- `Assets/StreamingAssets`

#### Hidden Assets

During the import process, Unity completely ignores the following files and folders in the Assets folder (or a sub-folder within it):

- Hidden folders.
- Files and folders which start with ‘.’
- Files and folders which end with ‘~’
- Files and folders named cvs
- Files with the extension .tmp

## Additional Resources

- [Is there a standard/recommended directory structure for Unity projects?](https://stackoverflow.com/questions/44363854/is-there-a-standard-recommended-directory-structure-for-unity-projects/45095619)
    - [Mastering Unity Project Folder Structure. Level 2 – Assets Organization](http://developers.nravo.com/mastering-unity-project-folder-structure-level-2-assets-organization/)
    - [50 Tips for Working with Unity (Best Practices)](http://devmag.org.za/2012/07/12/50-tips-for-working-with-unity-best-practices/)
    - [Unity Forums: Best practices - Folder structure](http://www.arreverie.com/blogs/unity3d-best-practices-folder-structure-source-control/)
- [7 Ways to Keep Your Unity Project Organized](https://blog.theknightsofunity.com/7-ways-keep-unity-project-organized/)
- [Move Plugin Code to "Plugins"](https://connect.unity.com/p/move-plugin-code-to-plugins)