# 3D4AR
Augmented Reality 3D models visualization

Unity3D Settings
For versions of Unity 3D v4.3 and up:

(Skip this step in v4.5 and up) Enable External option in Unity → Preferences → Packages → Repository.
Switch to Visible Meta Files in Edit → Project Settings → Editor → Version Control Mode.
Switch to Force Text in Edit → Project Settings → Editor → Asset Serialization Mode.
Save the scene and project from File menu.

Additional Configuration
One of the few major annoyances one has with using Git with Unity3D projects is that Git doesn't care about directories and will happily leave empy directories around after removing files from them. Unity3D will make *.meta files for these directories and can cause a bit of a battle between team members when Git commits keep adding and removing these meta files.

Add this Git post-merge hook to the /.git/hooks/ folder for repositories with Unity3D projects in them. After any Git pull/merge, it will look at what files have been removed, check if the directory it existed in is empty, and if so delete it.
