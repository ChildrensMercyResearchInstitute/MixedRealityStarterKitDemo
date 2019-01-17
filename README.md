# Mixed Reality Starter Kit Demo 
Contains a Unity 2018 project demonstrating  Children's Research Institute's Mixed Reality Starter Kit being used in conjunction with Microsoft's Mixed Reality Toolkit. The Mixed Reality Starter Kit is a reusable set of C# scripts and UI elements for quickly publishing apps that display interactive 3D holograms to Microsoft's HoloLens with little to no programming or scripting knowledge. The kit includes visual buttons, hand gestures, and voice commands for model rotation, resizing, hiding portions of a model, and undoing these actions. 

# Getting Started
1.	Installation process
	1. Clone or download this repository from GitHub.
	1. Clone or download Microsoft's Mixed Reality Toolkit from https://github.com/Microsoft/MixedRealityToolkit-Unity
	1. Clone or download Children's Research Institute's Mixed Reality Starter Kit from https://github.com/ChildrensResearchInstitute/MixedRealityStarterKit
    1. Use Windows Explorer to copy and paste the HoloToolkit and MixedRealityStarterKit folders into the Assets folder of the MixedRealityStarterKitDemo project:
        1. Copy the HoloToolkit folder, which you'll find inside the Assets folder included in the Microsoft MixedRealityToolkit's folder hierarchy.
        1. Paste the HoloToolKit folder into the Assets folder located in the MixedRealityStarterKitDemo's folder hierarchy.
        1. Copy the MixedRealityStarterKit folder from the Children's Research Institute MixedRealityStarterKit folder.
        1. Paste the MixedRealityStarterKit folder into the Assets folder located in the MixedRealityStarterKitDemo's folder hierarchy.
        1. The MixedRealityStarterKitDemo folder hierarchy should now look like this:

        ```
        MixedRealityStarterKitDemo\
        ├─── Assets\
            ├─── Branding\
            ├─── HoloToolKit\
            ├─── Materials\
            ├─── MixedRealityStarterKit\
            ├─── Models\
            ├─── Scenes\
        ├─── Library\
        ├─── Packages\
        ├─── ProjectSettings\
        ├─── Temp\
        Assembly-CSharp.csproj
        Assembly-CSharp-Editor.csproj
        MixedRealityRStarterKitDemo.csproj
        MixedRealityStarterKitDemo.Editor.csproj
        MixedRealityStarterKitDemo.Player.csproj
        MixedRealityStarterKitDemo.sln
        ```
    1. The MixedRealityStarterKitDemo project is now ready to build and test.

1.	Software dependencies
    1. Microsoft Windows 10 with Fall Creator's Update installed.
    1. Unity 2018.2.16f1, available here: https://store.unity.com/
    1. Visual Studio 2017 or higher, available here: https://www.visualstudio.com/downloads/
		1. Select the option to install Universal Windows Platform development tools when prompted by Visual Studio installer.
	1. Microsoft Mixed Reality Toolkit, available here: https://github.com/Microsoft/MixedRealityToolkit-Unity
	1. Children's Research Institute's Mixed Reality Starter Kit, available here: https://github.com/ChildrensResearchInstitute/MixedRealityStarterKit

# Build and Test

1. Connect the HoloLens to your PC via USB.
1. Open the MixedRealityStarterKitDemo project in Unity 2018:
    1. Launch Unity 2018.
    1. Click the Open button near the top right corner of the window that appears.
    1. Navigate to the MixedRealityStarterKitDemo folder.
    1.  Click Select Folder to open the MixedRealityStarterKitDemo project.
1. In Unity, click the File menu and select "Build Settings..."
1. In the Build Settings window that appears, click the Build button near the bottom right corner of the window.
1. In the window that appears, click once on the folder named "App"
1. Click the Select Folder button near the bottom corner of the window.
1. A progress bar will appear as Unity builds this project into a Visual Studio Solution, which will be used to publish the app to the HoloLens in the next steps.
1. A new Windows Explorer window will pop open when Unity is done building. 
1. Open the App folder in the window that appears.
1. Double-click the "MRSK Demo.sln" file inside the App folder to open it in Visual Studio.
1. Once Visual Studio is open, switch to Release mode, change the platform to x86, and change the build target to Device:
    1. Click the black downward pointing triangle next to the word Debug in the dropdown menu near the top of the screen and select Release.
    1. Click the black downward pointing triangle next to the word ARM in the dropdown menu near the top of the screen and select x86.
    1. Click the black downward pointing triangle next to the word Local Machine in the dropdown menu near the top of the screen and select Device.
1. Click the green triangle to the left of the word Device in the dropdown menu near the top of the screen to build and deploy the app to your HoloLens. The Output panel near the bottom of the Visual Studio screen will display build and deployment progress.
1. Put on your HoloLens while you wait for build and deployment to complete. The app should launch automatically. See the troubleshooting section below for common error messages and guidance.

# Troubleshooting
1. Build and Deploy issues:
    1. Visual Studio Error: Access is denied
        - Typically, this error indicates that the app did build and deploy successfully, but Visual Studio was unable to launch the app on the HoloLens automatically for some reason. In our experience, as long as Visual Studio's build output window shows build and deploy were successful, you should be able to put on the HoloLens and launch the app.
        - Potential Resolution 1: Uninstall the app from the HoloLens, then use Visual Studio to build and deploy the app again.
        - Potential Resolution 2: Delete the App folder that contains the Visual Studio solution, create a new, empty App folder in its place, and redo all Build and Deploy steps above.
    1. Visual Studio Error: Could not deploy while a user-defined section is open
        - We tend to see this error when we are repeatedly building and deploying to HoloLens after making small adjustments to our Unity scene or scripting. If you see this error, your Visual Studio project did not build and deploy to the HoloLens properly.
        - Potential Resolution 1: Clean the Visual Studio solution and try running the app without debugging again. 
        - Potential Resolution 2: Delete the App folder that contains the Visual Studio solution, create a new, empty App folder in its place, and redo all Build and Deploy steps above.

# Demo Videos

1. https://www.youtube.com/watch?v=O6x1AsDEqno
2. https://www.youtube.com/watch?v=CEtRWAKekWA
3. https://www.youtube.com/watch?v=0jjTI3yN78w
