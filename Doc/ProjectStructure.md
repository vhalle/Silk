# Folder Structure

## Unity Special Folder

[Official Documentation](https://docs.unity3d.com/Manual/SpecialFolders.html)

> You can usually choose any name you like for the folders you create to organise your Unity project. However, there are a number of folder names that Unity interprets as an instruction that the folder’s contents should be treated in a special way.

### Regular Folders

- `Assets/*/Editor`
- `Assets/*/Resources`

### Unique Folders

- `Assets/Editor Default Resources`
- `Assets/Gizmos`
- `Assets/Standard Assets`
- `Assets/StreamingAssets`

### Hidden Assets

During the import process, Unity completely ignores the following files and folders in the Assets folder (or a sub-folder within it):

- Hidden folders.
- Files and folders which start with ‘.’
- Files and folders which end with ‘~’
- Files and folders named cvs
- Files with the extension .tmp