# TrenchBroom Installation & Setup for Quake 2 Remastered

After completing this guide, you will be ready to create Quake 2 Remastered maps using the TrenchBroom map editor.
## Table of Contents

+ [Video Guide](#video)
+ [Getting Started](#getting_started)
+ [Prerequisites](#prerequisites)
+ [Section 1 - Installing TrenchBroom](#section1)
+ [Section 2 - Find your Quake 2 Steam folder location](#section2)
+ [Section 3 - Copying Quake 2 Files into TrenchBroom](#section3)
+ [Section 4 - Configuring Quake 2-RE game engine preferences in TrenchBroom](#section4)
+ [Section 5 - Compile Setup](#section5)
+ [FAQ](#faq)
+ [Authors](#authors)
+ [Acknowledgments ](#acknowledgments)

## Video Guide <a name = "video"></a>

The information in this guide is also presented in the initial 11 minutes of the video below linked below.
[Quake 2 Remaster Mapping Tutorial - Part 1: Setup and first map](https://www.youtube.com/watch?v=jDyfpSgnjDc)
## Getting Started <a name = "getting_started"></a>

We'll need to install the TrenchBroom map editor, copy some files and then install ericw-tools. The following steps will guide you through this process.

**Note**: This installation guide covers both Steam and GOG versions of Quake 2 Remastered. 
- Steam specific instructions are labeled as **->Steam**.
- GOG specific instructions are labeled as **->GOG**.
## Prerequisites <a name = "prerequisites"></a>

- **Windows Operating System**
- **Microsoft Visual C++ Redistributable** for Visual Studio 2015, 2017 and 2019
	- [x86 version](https://aka.ms/vs/16/release/vc_redist.x86.exe) for running 32-bit TrenchBroom
	- [x64 version](https://aka.ms/vs/16/release/vc_redist.x64.exe) for running 64-bit TrenchBroom  
	**Note**: *Not sure which one? Try the x64 version first.*
- **Quake 2 from Steam or GOG**
	- **Steam version** - Purchased [here](https://store.steampowered.com/app/2320/Quake_II/)
	- **GOG version** - Purchased [here](https://www.gog.com/en/game/quake_ii_quad_damage)
- **7zip** or **WinRAR** - Apps needed for decompressing the .7z file format -  [Get 7zip](https://www.7-zip.org/download.html) [Get WinRAR](https://www.win-rar.com/predownload.html?&L=0)

## Section 1 - Installing TrenchBroom <a name = "section1"></a>
How to install TrenchBroom on a Windows PC, step by step.

1. Navigate to the TrenchBroom GitHub release page.
	- Located at https://github.com/TrenchBroom/TrenchBroom/releases or by clicking [here](https://github.com/TrenchBroom/TrenchBroom/releases).

2. Find the latest version post (usually at the top) and scroll down to the **Assets** section. You'll find the TrenchBroom download links there.  
	**Note**: If you can't find it, locate the download links at the bottom of the latest release post and try expanding the list by clicking the word "Assets". GitHub can hide this section by default.

3. Click "TrenchBroom-Win64-vXXXX-Release.7z" to begin downloading the TrenchBroom application. (If you know you're running 32bit Windows, download the Win32 version instead.)
		Example GitHub download link for Windows 64bit:
		<p align="left">
  		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694641558754.jpeg?raw=true" 			
		alt="TrenchBroom Download Link Example">
		</p>

4. Extract the contents of the downloaded .7z file to any folder on your system.
	-> Not sure what this means? Perform the following steps:  
&emsp;&emsp;1. Create a folder on your Desktop or in your Documents folder and name it "TrenchBroom".  
&emsp;&emsp;2. Open the .7z file, select every file within, and drag them to the TrenchBroom folder you created. That's it! Your installation is now complete!  
&emsp;&emsp;**Note**: *If you're unable to open the 7z file, it's possible you forgot to download 7zip or WinRAR (seen in the Prerequisite section above).* If you're not sure which, grab 7zip for simplicity sake.

## Section 2 - Find your Quake 2 Steam folder location <a name = "section2"></a>
We'll need to copy some files starting in Section 3. First, locate your Quake 2 Steam installation file path using the steps below.

**Note**: *If you already know your Quake 2 installation file path, then skip to Section 3.*

1. Locate "Quake 2" in your steam library, then **right-click** on it to open its context menu.

2. Click "Properties..."
		<p align="left">
  		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694641844649.jpeg?raw=true" 			
		alt="Quake 2 Steam Properties">
		</p>

3. Within the Properties menu, click on the "Installed Files" tab near the left side.

4. Then click on the "Browse..." button on the right side to open the Quake 2 installation folder.
		<p align="left">
  		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694641921508.jpeg?raw=true" 			
		alt="Browse Steam Quake 2 Files">
		</p>
5. Once the Quake 2 folder opens, click the folder icon on the left side of the address bar. This action will reveal the complete file path, which you should copy and store for use in Section 3.
		<p align="left">
		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694642018602.jpeg?raw=true" 	
		alt="Click on folder icon to reveal Quake 2 file path.">
		</p>

	<p align="left">
  	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694642066522.jpeg?raw=true" 
	alt="copy quake 2 file path">
	</p>

## Section 3 - Copying Quake 2 Files into TrenchBroom <a name = "section3"></a>
We need to copy all the files from "Quake 2\\rerelease\\fgd" to "TrenchBroom\\games\\Quake2RE", then make a minor modification to one of the copied files. The following steps will guide you through this process.

1. Navigate to your Quake 2 Steam installation folder (found in Section 2).

2. Open the "rerelease" folder.  
**Note**: *Pin this folder to quick access to easily find it again. You will need it in later steps.*

3. Open the "fgd" folder.

4. Select and copy all 4 files.
	<p align="left">
	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694642147523.jpeg?raw=true" 
	alt="Copy files from Quake2/rerelase/fgd">
	</p>

5. Navigate to the TrenchBroom folder (created in Section 1).

7. Open the **Games** folder.

9. Create a new folder and name it **Quake2RE**.  
	**Note**: *This folder can have any name. We recommend Quake2RE for simplicity.*

8. Paste all 4 files copied from Step 4 into this new folder.
	<p align="left">
  	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694642259914.jpeg?raw=true" 
	alt="Paste files into TrenchBroom\games\Quake2RE">
	</p>

9. Inside the "TrenchBroom\games\Quake2RE" folder, open the "GameConfig.cfg" text file. If prompted to choose an application to open GameConfig.cfg, perform the following steps to open it in Notepad:  
&emsp;&emsp;1. Select **Notepad**  
&emsp;&emsp;2. Click the "Always" button.
		<p align="left">
  		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694642395691.jpeg?raw=true" 			
		alt="Choose Notepad, then click always">
		</p>

10. Within the GameConfig.cfg text file, locate the line shown below.
  
	```"name": "Quake 2",```
  
	Replace it with:
  
	```
	"name": "Quake 2-RE",
 	```
  
	So that it looks like:  
 	<p align="left">
  	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694642421530.jpeg?raw=true" 			
	alt="Replace 'Quake 2' with 'Quake 2-RE'">
	</p>

12. After the edit, save and close the GameConfig.cfg text file.

13. Copy the Quake 2 icon file over to the Quake2RE folder by performing the following steps:  
&emsp;&emsp;1. Navigate to "TrenchBroom\\games\\Quake2"  
&emsp;&emsp;2. Copy "Icon.png"  
&emsp;&emsp;3. Navigate to "TrenchBroom\\games\\Quake2RE"  
&emsp;&emsp;4. Paste "Icon.png"

## Section 4 - Configuring Quake 2-RE game engine preferences in TrenchBroom <a name = "section4"></a>

We'll need to tell TrenchBroom where it can find your Quake 2-RE files. The following steps will walk you through that process.

1. Open the TrenchBroom folder you created back in Section 1.

2. Locate TrenchBroom.exe and run it by double-clicking the file.  
		**Note**: *The ability to see file extensions may be turned off for your system. If so, simply double-click on the file that is labeled TrenchBroom to launch the application.*
		<p align="left">
  		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694642504548.jpeg?raw=true" 			
		alt="Open Trenchbroom.exe">
		</p>

3. A "Welcome to TrenchBroom" window should appear, displaying two buttons: **New Map** and **Browse**.

4. Click on the **New Map** button.
	<p align="left">
  	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694644941181.jpeg?raw=true" 
	alt="New Map 	button">
	</p>

5. Within the "Select Game" menu, perform the following steps:  
&emsp;&emsp;1. On the right side, use the scroll bar or mouse wheel to locate and select "Quake 2-RE".  
&emsp;&emsp;2. Click on the **Open preferences...** button.
	<p align="left">
  	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694643150738.jpeg?raw=true" 
	alt="Select Quake 2 RE and click Preferences">
	</p>

6. Within the Preferences window, perform the following steps:  
&emsp;&emsp;1. Select "Quake 2-RE" on the left side.  
&emsp;&emsp;2. For Game Path, input the file path to your Quake 2 Steam rerelease folder. (Default: C:\\Program Files (x86)\\Steam\\steamapps\\common\\Quake 2\\rerelease)  
&emsp;&emsp;**Note:** *If you pinned this rerelease folder back in Section 3 - Step 2, then click on that to go directly there. Copy the file path to this folder.*  
&emsp;&emsp;3. Click the **Configure engines..** button.
	<p align="left">
  	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694643226920.jpeg?raw=true" 
	alt="Update Game Path for Quake 2 RE and then click configure engines ">
	</p>

7. Within the "Game Engines" window, perform the following steps:  
&emsp;&emsp;1. Click on the **+** button to create a new profile.  
&emsp;&emsp;2. In the "Name" text box, input "Quake 2-RE".  
&emsp;&emsp;3. In the Path text box, input your system's file path to "Steam.exe".  
&emsp;&emsp;**Note**: *If you do not know where where Steam.exe is, then try the default file path: C:\\Program Files (x86)\\Steam\\steam.exe*  
&emsp;&emsp;4. Click the "Close" button.
	<p align="left">
  	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694643822350.jpeg?raw=true" 
	alt="Create Quake 2 RE profile, then input you file path to steam.exe">
	</p>

8. At the "Preferences" window, perform the following steps:  
&emsp;&emsp;1. Click **Apply** to save your changes.  
&emsp;&emsp;2. Click **OK** to leave the "Preferences" window.  

9. At the "Select Game" window perform the following steps:  
&emsp;&emsp;1. Ensure that the Quake 2-RE entry is selected.  
&emsp;&emsp;2. Always choose "Quake2 (Valve)" within the Map Format dropdown menu.  
&emsp;&emsp;**Note**: *You may need to choose "Quake 2 (Valve)" each time you create a new map.*  
&emsp;&emsp;3. Click the **OK** button to launch the TrenchBroom editor.
		<p align="left">
  		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694643859796.jpeg?raw=true" 			
		alt="Map format should always be 'Quake 2 (Valve)''">
		</p>

10. The TrenchBroom editor should now be open. To confirm that it's set up with Quake 2 Remastered, we'll need to see if we can find its entities. We can do this by performing the following steps:  
&emsp;&emsp;1. Click on the "Entity" tab within the panel near the right side.  
&emsp;&emsp;2. If you can see 3D models populating the Entity browser, then you're ready to move onto Section 5.
	<p align="left">
 	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694643896613.jpeg?raw=true" 
	alt="Entity Browser">
 	</p>

## Section 5 - Compile Setup <a name = "section5"></a>
TrenchBroom is up and running with Quake 2 Remastered, but we're not done yet. Now we need to install compiling tools to generate the maps you create. To do this, we'll install ericw-tools and configure TrenchBroom to use them. The following steps will guide you through this process.

1. Navigate to the ericw-tools GitHub release page.
	- Located at https://github.com/ericwa/ericw-tools/releases or by clicking [here](https://github.com/ericwa/ericw-tools/releases).

2. Find the latest version post (usually at the top) and scroll down to the **Assets** section. You'll find the ericw-tools download links there.  
**Note**: *If you can't find it, locate the download links at the bottom of the latest release post and try expanding the list by clicking the word "Assets". GitHub can hide this section by default.

3. Click "ericw-tools-vXXXX-win64.zip" to begin downloading.  
&emsp;&emsp;Example GitHub download link for Windows 64bit:
		<p align="left">
  		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694643959036.jpeg?raw=true" 			
		alt="ericw-tools download link example">
		</p>

4. Extract the ericw-tools zip file to any location on your PC and make a note of its file path.

5. Launch TrenchBroom and open up "Compile Map" settings by performing the following steps:  
&emsp;&emsp;1. Click the "Run" dropdown menu near the top.  
&emsp;&emsp;2. Click on "Compile Map..."
		<p align="left">
  		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694643980436.jpeg?raw=true" 			
		alt="click Run, then click Compile map">
		</p>

6. Within the Compile window, perform the following steps:  
&emsp;&emsp;1. Locate the Profile section on the left side and click the **+** button near the bottom left to create a new profile.  
&emsp;&emsp;2. Input the following "Name" and "Working Directory" text for the new profile.  
&emsp;&emsp;&emsp;- **Name**: ```Quake 2 RE (fast)```  
&emsp;&emsp;&emsp;- **Working Directory**: ```${MAP_DIR_PATH}```  
&emsp;**Note**: *This profile will have the (fast) label because it will be your quick compile option. Lower quality lighting but much faster to compile maps for testing.*  
		<p align="left">
  		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694644060493.jpeg?raw=true" 			
		alt="Quake 2 (lite) compile profile">
		</p>

7. Locate the "Details" section near the right side and click the + button near the bottom, then choose "Run Tool" from the dropdown menu.
		<p align="left">
  		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694644101701.jpeg?raw=true" 			
		alt="Create Run Tool Entries">
		</p>

8. Repeat this step until you have 3 empty "Run Tool" entries listed within the "Quake 2 RE (fast)" profile you just created.
	<p align="left">
  	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694644396915.jpeg?raw=true" 
	alt="Three empty run tools entries shown">
	</p>

9. Populate the "Tool Path" and "Parameter" text boxes for each "Run Tool" entry by performing the following steps:
  
&emsp;&emsp;**Note**: *To input the correct "Tool Path" for your system, you will need to know where you extracted ericw-tools* back in Step 4.
  
&emsp;&emsp;1. Run Tool #1  
  
&emsp;&emsp;&emsp;**Tool Path**:
  
&emsp;&emsp;&emsp;```ericw-tools-win64/bin/qbsp.exe```  
  
&emsp;&emsp;&emsp;**Parameters**: 
  
```
-nostat -nopercent -q2bsp ${MAP_BASE_NAME}
```  
&emsp;&emsp;2. Run Tool #2  
  
&emsp;&emsp;&emsp;**Tool Path**: 
  
&emsp;&emsp;&emsp;```ericw-tools-win64/bin/vis.exe```  
  
&emsp;&emsp;&emsp;**Parameters**: 
  
```
${MAP_BASE_NAME}
```  
&emsp;&emsp;3. Run Tool #3  
  
&emsp;&emsp;&emsp;**Tool Path**: 
  
&emsp;&emsp;```ericw-tools-win64/bin/light.exe```  
  
&emsp;&emsp;&emsp;**Parameters**: 
  
```
-nostat -dirt -world_units_per_luxel 24 -wrnormals -novanilla -lightgrid -lightgrid_dist 64 64 64 ${MAP_BASE_NAME}
```  
<p align="left">
<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694644731979.jpeg?raw=true" 
alt="Three Run Tool entries fully configured.">
</p>

10. Next we'll create our **Full** lighting compile option. Perform the following steps:  
&emsp;1. Right-click on the "Quake 2 RE (fast)" profile near the upper left, then click on the "Duplicate" option.  
	<p align="left">
  	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694644783122.jpeg?raw=true" 
	alt="How to duplicate a profile">
	</p>

&emsp;&emsp;&emsp;2. Replace the word "fast" in "Quake 2 RE (fast)" with the word "full". So that it displays Quake 2 RE (Full).  
  
&emsp;**Note**: *This profile will have the (full) label because it will be your slow compile option. Higher quality lighting but slower to compile maps. Best to use when finalizing the lighting or as your last compile before releasing the map itself.*  
	<p align="left">
  	<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694644831683.jpeg?raw=true" 
	alt="Quake 2 RE (full) compile profile">
	</p>
&emsp;&emsp;3. Within the "Quake 2 RE (full)"" profile, update the parameters on Run Tool #3 using the line below. Do not update Run Tool #1 and #2.    
    
&emsp;&emsp;&emsp;Run Tool #3 Parameters: 

```
-emissivequality high -nostat -dirt -extra4 -world_units_per_luxel 8 -wrnormals -novanilla -lightgrid -lightgrid_dist 32 32 32 ${MAP_BASE_NAME}
```

11. To launch Quake 2 Remastered directly from TrenchBroom, you'll need to configure the launch parameters. Perform the following steps:  
&emsp;&emsp;1. Within the Compile window, click on the "Launch..." button at the bottom.  
		<p align="left">
  		<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694644854810.jpeg?raw=true" 			
		alt="Launch button">
    		</p>
&emsp;&emsp;2. This opens the "Launch Engine" window. Choose whether you wish to create single player or multiplayer maps, then input the the respective parameter:
   
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;- Parameters for Single Player maps:  
  
```
-applaunch 2320 -skipmovies +bind f10 "quit" +map ${MAP_BASE_NAME} +set cheats 1
```  

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Or  
  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;- Parameters For Multiplayer maps:  
  
```
-applaunch 2320 -skipmovies +bind f10 "quit" +map ${MAP_BASE_NAME} +set cheats 1 +set deathmatch 1
```  

<p align="left">
<img src="https://github.com/eKioga/Technical_Writing/blob/main/Tutorials/Quake2-RE/TrenchBroom/assets/part1/Part%201%20-%20Trenchbroom%20Install-1694644892683.jpeg?raw=true" 
alt="Launch Engine Parameters">
</p>

12. Close the "Launch Engine" and "Compile" windows.

**TrenchBroom is now set up for making maps for Quake 2 Remastered. Congratulations!**

## FAQ <a name = "faq"></a>
- How can I enable dark mode?  
&emsp;&emsp;1. Within the TrenchBroom map editor, click the "View" dropdown menu at the top, then click on "Preferences".  
&emsp;&emsp;2. At the top of the "Preferences" window click the "View" tab.  
&emsp;&emsp;3. The "User Interface" section at the top displays a Theme dropdown menu. Select the "Dark" option.  
&emsp;&emsp;4. Restart TrenchBroom  
- How can I find key bindings for TrenchBroom?  
&emsp;&emsp;1. Within the TrenchBroom map editor, click the "View" dropdown menu at the top, then click on "Preferences".  
&emsp;&emsp;2. At the top of the "Preferences" window click the "Keyboard" tab.  
&emsp;&emsp;3. Use the search feature near the lower right corner or scroll down the window to view all key bindings.  

# Authors <a name = "authors"></a>
- Kioga - Initial writing, editing and annotated screenshots.
- PalmliX - Created the video series that informs this documentation.
- Paril - Provided compile commands and technical support
- xaGe - Provided Trenchbroom Steam launch commands and technical support

# Acknowledgments <a name = "acknowledgments"></a>
- A huge thanks to both PalmliX and Grue. Both serve as an inspiration for me and the Quake 2 mapping community.
