# Table of Contents
<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/4b02dde0-bc11-4659-9413-c5134fdcd1c7" height="32" width="32"/></td>
    <td><a href="#section-1---loading-screens-3"><b>Section 1 - Loading Screens &lt;3 </b></a></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/16f48b7d-c44e-4e97-802a-5ccddd56b60e" height="32" width="32"/></td>
    <td><a href="#section-2---music-system-3"><b>Section 2 - Music System &lt;3</b></a></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/4b02dde0-bc11-4659-9413-c5134fdcd1c7" height="32" width="32"/></td>
    <td><a href="#section-3---settings-menu-3"><b>Section 3 - Settings Menu &lt;3 </b></a></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/16f48b7d-c44e-4e97-802a-5ccddd56b60e" height="32" width="32"/></td>
    <td><a href="#section-4---environment-3"><b>Section 4 - Environment &lt;3</b></a></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/4b02dde0-bc11-4659-9413-c5134fdcd1c7" height="32" width="32"/></td>
    <td><a href="#section-5---text-chat-3"><b>Section 5 - Text Chat &lt;3 </b></a></td>
  </tr>
</table>

<br>


# Section 1 - Loading Screens <3

> Before we begin, your ReplicatedFirst folder should look like this.  
> <img width="411" height="58" alt="image" src="https://github.com/user-attachments/assets/9a24df2b-4238-41fe-b89d-c89b5638bbc2" />  
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.


### Configuration Part 1 (Config Values)  
<img width="229" height="180" alt="image" src="https://github.com/user-attachments/assets/e249b792-cfc6-4ad7-bfb7-36b8fd2a0aee" /><br>
The image above represents all possible Loading screen configs for Rose of Sharon (RS)  
Here is a breakdown of all properties in a sorted table.  
| Config Property | Value Type | Explanation |
| :---: | :---: | :---: |
| SoundStartID | SoundID | **Plays a SoundID** while the loading screen animation of the icon just begins.<br>Default is```nil``` |
| LoadingScreenEnabled | boolean | Determines whether to **begin the loading screen or disable** it entirely<br>Default is```true``` |
| IconAssetID | TextureID | Inserts a **TextureID to the main icon** during the loading screen animation<br><img width="150" height="150" alt="An example of the icon display on the loading screen" src="https://github.com/user-attachments/assets/f292d962-5128-49ae-ba20-0e5ecd258180" /><br>e.g. this has ```IconAssetID = "rbxassetid://73439321896937"``` |
| CreditsShown | boolean | Whether to display **Credits** on the developer console (F9)<br><img width="1121" height="135" alt="The Developer Console Credits Input" src="https://github.com/user-attachments/assets/a817353b-4ca0-4b6f-93e7-b2c759663520" /><br>e.g. this has ```CreditsShown = true``` |
| ParticlesOnIcon | boolean | Whether to display **Expanding Particle VFX** in the loading screen animation<br><img width="1393" height="793" alt="image" src="https://github.com/user-attachments/assets/ecb99d3f-1758-4224-80b1-b75c5f4b01ec" /><br>e.g. this has ```ParticlesOnIcon = true``` |
| ParticleColor | Color3 | Determines whether what **RGB Value** the expanding particles should be default is<br>```Color.fromRGB(255,255,255)``` |
| NumberOfParticles | integer | Determines **how much particles** should be rendered in the **Expanding Particle VFX.**<br><img width="1440" height="788" alt="image" src="https://github.com/user-attachments/assets/2cc50c12-b838-4433-9136-02821b6e90cc" /><br>e.g this has ```NumberOfParticles = 1``` |


### Configuration Part 2 (ExtraConfigs)
<img width="518" height="376" alt="image" src="https://github.com/user-attachments/assets/6ac1d42c-af09-4b31-8964-a7d5ad333ac1" /><br>
The image above represents all possible Loading Screen **ExtraConfigs** for Rose of Sharon Extras (RSE)  
Here is a breakdown of all properties in a sorted table.  
| Config Property | Value Type | Explanation |
| :---: | :---: | :---: |
| InitialIconSize | [UDim2](UDim12.md) | Sets the **Size of the icon initially** right as the loading animation plays.<br><img width="737" height="678" alt="image" src="https://github.com/user-attachments/assets/89d559bb-8f18-49de-be2b-6825ee16e6e6" /><br>e.g. this has ```InitialIconSize = UDim2.new(0.15,0,0.15,0)``` |
| VertexIconSize | [UDim2](UDim12.md) | Sets the **Size of the icon** right at its largest point when the loading animation is in the middle of completion.<br><img width="790" height="785" alt="image" src="https://github.com/user-attachments/assets/a3ea1e49-7184-4a06-91d7-1dc9bdcbdf8e" /><br>e.g. this has ```InitialIconSize = UDim2.new(14/15,0,14/15,0)``` |
| SetInIconSize | [UDim2](UDim12.md) | Sets the **Size of the icon** after the boot up animation has been completed.<br><img width="783" height="747" alt="image" src="https://github.com/user-attachments/assets/56ef3462-c41d-4565-b154-b4167caa9662" /><br>e.g. this has ```InitialIconSize = UDim2.new(7/9,0,7/9,0)``` |
| IconUICornerRadii | List of **[UDim](UDim12.md)** | **A list of 4 corners defined as ```TopLeftRadius,TopRightRadius,BottomLeftRadius,BottomRightRadius``` with [UDim](UDim12.md) values.** I suggest visiting the UDim12.md documentation for more depth about them!<br><img width="379" height="369" alt="image" src="https://github.com/user-attachments/assets/3a7a9ebc-0145-4673-b11d-35ae48ea4be4" /><br>e.g. this Icon uses these **[UDim](UDim12.md)** parameters below:<br><img width="311" height="85" alt="image" src="https://github.com/user-attachments/assets/ee4e8def-34df-406b-8030-3607489b4678" /> |
| UITextFontFace | Enum.Font | Sets the rendered font of all status texts from a **predefined list of Enum.Font fonts**<br><img width="203" height="43" alt="image" src="https://github.com/user-attachments/assets/0f534430-c7b9-46b9-bf3d-46067cb34e88" /><br>e.g. this status text uses ```UITextFontFace = Enum.Font.IndieFlower``` |
| UITextFontStyle | Enum.FontStyle | Sets the font style of all status texts, which can be either **Normal or Italicized** <br><img width="416" height="108" alt="image" src="https://github.com/user-attachments/assets/f7c365f9-f1a8-40d0-b757-22c8f5fc9e8e" /><br>e.g. this button uses ```UITextFontStyle = Enum.FontStyle.Italic``` |
| UITextFontWeight | Enum.FontWeight | Sets the font weight of all status texts, which can range from **Super Skinny Light to Heavy Black**.<br><img width="255" height="38" alt="image" src="https://github.com/user-attachments/assets/696927b0-0e6f-411a-a3c6-39202a9c8c73" /><br>e.g. This status text uses ```UITextFontWeight = Enum.FontWeight.Bold``` |
| BackgroundBlack | Color3 | Determines the **Color3 value** of the **black contrasted side of the loading screen.**<br>Default is```Color.fromRGB(0,0,0)``` |
| BackgroundWhite | Color3 | Determines the **Color3 value** of the **white contrasted side of the loading screen.**<br>Default is```Color.fromRGB(255,255,255)``` |


### Configuration Part 3 (Misconceptions & Traps)
One common misconception i see is people blindly pasting **IconAssetID/SoundStartID** into the string field and then complain why the icon/sound wont play. This is because it is not a valid **SoundID or TextureID** in the eyes of roblox. To correct paste in the correct id, here are both demo videos below of how i like to paste my ids to get the correct string for the parser :D
| SoundID | TextureID |
| :---: | :---: |
| <video src="https://github.com/user-attachments/assets/22f77ee9-d0a6-43b2-8907-5b3cc538d737" controls></video> | <video src="https://github.com/user-attachments/assets/cb70d145-6349-41e9-80e0-a67eca242952" controls></video><br> |

Once you have the ```rbxassetid://1234567890``` you can paste it into the **IconAssetID/SoundStartID** fields and it will finally be fixed >~<


Another misconception is ___please dont set NumberOfParticles to 0 or any negative integer___. This will obviously break the loading screen TwT. ___and definitely dont set NumberOfParticles to a giant number like 1,346,549,200___ your pc fans will hate u<br>
And also if your configurations dont match this AND especially the **module script**<br>
<img width="229" height="180" alt="image" src="https://github.com/user-attachments/assets/e249b792-cfc6-4ad7-bfb7-36b8fd2a0aee" /><br>
<img width="518" height="376" alt="image" src="https://github.com/user-attachments/assets/6ac1d42c-af09-4b31-8964-a7d5ad333ac1" /><br>
Then you may want to add the proper values back or redo instructions on [The Installation Guide](Installation.md)

ONE Thing about Color3, A new Color3 Value created from Color3.new must have rgb values from [0,1]. While Color3.fromRGB must be from [0,255]!

Also Also, some IconAssetID/SoundStartID may not work because **the asset is entirely private/got taken down or DMCAed**


# Section 2 - Music System <3

> Before we begin, your ReplicatedStorage folder should atleast contain ```RoseOfSharonConfig```.  
> <img width="189" height="140" alt="image" src="https://github.com/user-attachments/assets/e88355e9-d1c3-44c8-935c-35681e36d3d1" /><br>
> And inside that ModuleScript it should look like this.<br>
> <img width="372" height="252" alt="image" src="https://github.com/user-attachments/assets/66593d54-54a9-4e1d-8656-8398d68052bc" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.

### Configuration Part 1 (Everything Else Besides the Soundtracks table)  
<img width="280" height="168" alt="image" src="https://github.com/user-attachments/assets/b32714cb-a90d-4c01-bea0-1349a5596a87" /><br>
The image above represents some Music System configs for Rose of Sharon (RS)  
Here is a breakdown of all properties in a sorted table.  
| Config Property | Value Type | Explanation |
| :---: | :---: | :---: |
| SongSystemBool | boolean | Determines whether if a song system and music sounds should be played<br><img width="560" height="145" alt="image" src="https://github.com/user-attachments/assets/1ce0bcfd-7a14-4e73-9f28-2c56ec7852df" /><br>e.g. the Music Settings Toggle appears when ```SongSystemBool = true``` |
| SFXToggleBool | boolean | Determines whether to display the SFX Toggle under settings<br><img width="568" height="76" alt="image" src="https://github.com/user-attachments/assets/d374325c-4f49-466d-8175-a098e6d48ae8" /><br>e.g. This appears when ```SFXToggleBool = true``` |
| CanPlayersChangeMusic | boolean | Sets if players can change the songs using both arrows<br><img width="477" height="80" alt="image" src="https://github.com/user-attachments/assets/93ab71bd-0ba1-4241-9232-12c230ec354f" /><br>e.g. The buttons appear when ```CanPlayersChangeMusic = true``` |
| CanPlayerSwitchPlaylists | boolean | Sets if players can change the playlists containing multiple songs as defined by the <a href="#configuration-part-2-the-soundtrack-table"><b>Soundtrack table</b></a><br><img width="568" height="94" alt="image" src="https://github.com/user-attachments/assets/6be228a8-344d-4929-8da6-2c0c7b6f6609" /><br>e.g. This appears when ```CanPlayerSwitchPlaylists = true``` |
| ShufflePlaylists | boolean | Whether you want that everytime the player rejoins the game, they get there playlist shuffled. e.g. when ```ShufflePlaylists = true``` whenever i rejoin, the playlist i get might not be the same as the one i had before i rejoined. If ```ShufflePlaylists = false```, then the playlist does not change randomly when i rejoin and instead it saves my **previous playlist I last had** |
| ShuffleSongs | boolean | Whether you want that everytime the song ends, a random new song **(from that specific playlist)** plays and does not repeat the same song. If ```ShuffleSongs = false``` then instead it plays in a sequential pattern **(defined by the <a href="#configuration-part-2-the-soundtrack-table"><b>Soundtrack table</b></a>)** regardless if you rejoin or not. |
| MasterVolume | number | Sets as the volume multiplier for Every song in every playlist<br><img width="526" height="40" alt="image" src="https://github.com/user-attachments/assets/3ec3d3dc-5751-48e5-b611-ab84c03ca5fd" /><br>e.g. This song with an original ***0.5 volume*** has ballooned to ***5.5 volume*** because ```MasterVolume=11``` |
| SFXMasterVolume | number | Sets as the volume multiplier for Every **Sound FX**<br><img width="157" height="161" alt="image" src="https://github.com/user-attachments/assets/04f6cae8-a5dc-405d-a8f8-cadfe8cedad3" /><br>e.g. when ```SFXMasterVolume = 2``` every sound will have its **volume 2x** |


### Configuration Part 2 (The Soundtrack table)  
<img width="390" height="548" alt="image" src="https://github.com/user-attachments/assets/9af0b197-2edc-48b6-9352-939feac663d1" /><br>
This image represents the Soundtrack nested table structure for Rose of Sharon (RS).<br>
It looks intimidating at first but here is a **breakdown of the entire structure.** <br>

```lua
Soundtracks = {
  ["Cutecore Playlist #1"] = {...}, --Songs go here.
  ["Cutecore Playlist #2"] = {...}, --Songs go here.
  ["Cutecore Playlist #3"] = {...}, --Songs go here.
  ["Cutecore Playlist #4"] = {...}, --Songs go here.
  ["Cutecore Playlist #5"] = {...}, --Songs go here.
  ["New Playlist"] = {}, --Step 1: Create a new playlist
}
```
So we begin by creating a **newline** and then declaring ```["New Playlist"] = {},```. The `"New Playlist"` defines the name of the playlist while the `{},` will define the **songs**. We then fill up the empty table by filling with this schema below
```lua
{
  Id = "rbxassetid://1234567890", --string
  Title = "The Song Name", --string
  Volume = 0.5, --number
},
```

We then put this entire table inside the `"New Playlist"` by formatting like this below
```lua
Soundtracks = {
  ["Cutecore Playlist #1"] = {...}, --Songs go here.
  ["Cutecore Playlist #2"] = {...}, --Songs go here.
  ["Cutecore Playlist #3"] = {...}, --Songs go here.
  ["Cutecore Playlist #4"] = {...}, --Songs go here.
  ["Cutecore Playlist #5"] = {...}, --Songs go here.
  ["New Playlist"] = {
    {
      Id = "rbxassetid://1234567890", --string
      Title = "The Song Name", --string
      Volume = 0.5, --number
    },
  },
}
```

We can also add multiple song entries like this
```lua
Soundtracks = {
  ["Cutecore Playlist #1"] = {...}, --Songs go here.
  ["Cutecore Playlist #2"] = {...}, --Songs go here.
  ["Cutecore Playlist #3"] = {...}, --Songs go here.
  ["Cutecore Playlist #4"] = {...}, --Songs go here.
  ["Cutecore Playlist #5"] = {...}, --Songs go here.
  ["New Playlist"] = {
    {
      Id = "rbxassetid://1234567890", --string
      Title = "The Song Name", --string
      Volume = 0.5, --number
    },
    {
      Id = "rbxassetid://1234567891", --string
      Title = "The Song Name 2", --string
      Volume = 0.5, --number
    },
    {
      Id = "rbxassetid://1234567892", --string
      Title = "The Song Name 3", --string
      Volume = 0.5, --number
    },
  },
}
```

So with that out of the way lets explain what `Id`, `Title` and `Volume` actually do :3
| Config Property | Id | Title | Volume |
| :---: | :---: | :---: | :---: |
| **Value Type** | SoundID | string | number |
| **Explanation** | **Plays the SoundID** used for the song entry. **Must be in `rbxassetid://` form**<br><img width="398" height="42" alt="image" src="https://github.com/user-attachments/assets/3ddcf67c-2292-43b5-a88b-a56d3ad8e9b4" /><br>e.g. this song has `Id = "rbxassetid://9047104411"` | Displays the Song Name in the radio<br><img width="477" height="80" alt="image" src="https://github.com/user-attachments/assets/93ab71bd-0ba1-4241-9232-12c230ec354f" /><br>e.g. this song has `Title = "Beach Cushions"` | **Adjusts the volume of the song** used for when a song is too quiet or too loud.<br><img width="282" height="16" alt="image" src="https://github.com/user-attachments/assets/83e49fbb-1183-4c8b-b846-c3487004ea4d" /><br>e.g. the song initially came out as too loud so it got set to `Volume = 0.5` |


### Configuration Part 3 (Misconceptions & Traps)  
One trap people make when setting up **playlists and song entries** and they finish there `{...}` they forgot to add a `,` to end of the table. Because if you dont have the `{...},` the script will break and not work. Also makes sure your song entry contains a `Id`, `Title` and a `Volume` AND they **must have a `,` after the declaration like e.g `Title = "Song Name",` <----**

The Script will also break if you make an empty playlist like this `["Empty Playlist"] = {},` please comment it out by doing `--["Empty Playlist"] = {},` or remove it entirely. While leaving a `Soundtracks = {},` wont break any code it is recommended to add atleast one placeholder even if you dont intend to play music.

And ofcourse if you did paste your `SoundID` yet it wont play or the script breaks. You can watch this video demo of how i like to get my `SoundID`<br>
<video src="https://github.com/user-attachments/assets/22f77ee9-d0a6-43b2-8907-5b3cc538d737" controls></video>

Also Also, some `SoundID` may not work because **the asset is entirely private/got taken down or DMCAed**


# Section 3 - Settings Menu <3

> Before we begin, your ReplicatedStorage folder should atleast contain ```RoseOfSharonConfig```.  
> <img width="189" height="140" alt="image" src="https://github.com/user-attachments/assets/e88355e9-d1c3-44c8-935c-35681e36d3d1" /><br>
> And inside that ModuleScript it should look like this.<br>
> <img width="852" height="738" alt="image" src="https://github.com/user-attachments/assets/358341e3-bafe-4816-88be-f8585ba675cb" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.


### Configuration Part 1 (Tips Config)  
Tips are a feature in our framework where it allows you to randomly display system messages with built in **RichText** or **Html parsing**. You can use this to promote your other games, outfits, ugc or remind people anything :3  

<img width="816" height="170" alt="image" src="https://github.com/user-attachments/assets/3c6bea1e-0ddb-44e7-be1b-628a0a012ac6" /><br>
The image above represents some Settings Menu configs for Rose of Sharon (RS)  
Here is a breakdown of all properties in a sorted table.  
| Config Property | Value Type | Explanation |
| :---: | :---: | :---: |
| ShowTips | boolean | Sets if you want to have occasional tips show in chat!<br><img width="465" height="80" alt="image" src="https://github.com/user-attachments/assets/e3bf7492-cc4b-4c8d-b047-893631a2dd63" /><br>e.g. This tip appears when ```ShowTips = true``` |
| SanitizeHtmlTags | boolean | Determines whether you want to enable **rich text formatting** via html tags.<br><img width="463" height="135" alt="image" src="https://github.com/user-attachments/assets/90e7e5e6-abe0-426b-8947-c1e318618190" /><br>e.g. the raw text for this when `SanitizeHtmlTags = false` is `<font size='44'>Please favorite and like the game! &lt;~&gt;</font>` |
| Tips | List of {Color3,string} | A defined list of `{Color3,string},` where the `Color3` can be set to any color and `string` is the actual message (tip).<br><img width="810" height="105" alt="image" src="https://github.com/user-attachments/assets/70432289-86b9-4e27-8de0-8c37b1d3fb41" /><br>Notice how theres a comma after every `{Color3,string}`, This is so the script doesnt break. |
| TipShowFrequency | number | Sets the period (in seconds) of when to display a randomized tip message. The Period is determined by `T*(1+r)` with r being a `random number from 0 to 1`<br><img width="468" height="266" alt="image" src="https://github.com/user-attachments/assets/03483192-2199-4f1e-b612-8a0dec004ce1" /><br>e.g. this happens when you set `TipShowFrequency = 0.3` |


### Configuration Part 2 (Settings Desc & Titles + Others)  
<img width="1027" height="356" alt="image" src="https://github.com/user-attachments/assets/3230e34e-836b-4b8c-8d79-560850552ad8" /><br>
The image above represents some Settings Menu configs for Rose of Sharon (RS)  
Here is a breakdown of all properties in a sorted table.  
| Config Property | Value Type | Explanation |
| :---: | :---: | :---: |
| SettingsTitleAndDesc | List of `{Title,Desc}` | This is a list containing all possible settings, you cannot remove or add any new elements. But you can **change the `Title` or `Desc` to any string** to your likings.<br><img width="545" height="72" alt="image" src="https://github.com/user-attachments/assets/5d8a702c-fa77-45c2-a74c-2e912bee59a7" /><br>e.g. This Music toggle had a modified `Music = {Title = "The Illuminati", Desc = "triangles"},` |
| AllowAFKToggle | boolean | Determines whether to display the AFK Toggle under settings **(DOES NOT AFFECT AFK STATUS)**<br><img width="553" height="67" alt="image" src="https://github.com/user-attachments/assets/e3e820f5-5b8c-4641-b0c9-36c26f121929" /><br>e.g. this AFK Toggle appears when ```AllowAFKToggle = true``` |
| AllowSprintingToggle | boolean | Determines whether to display the Sprint Toggle under settings. **(Note this will not affect sprinting itself only the toggle button)**<br><img width="547" height="72" alt="image" src="https://github.com/user-attachments/assets/451d5b8f-716e-40eb-bdd3-e9fccf04f4cb" /><br>e.g. this Sprint Toggle appears when ```AllowSprintingToggle = true``` |


### Configuration Part 3 (Setting Specific UI Configs)
These last config properties represent the UI portion of Settings, you can modify the colors of the on/off switches, buttons or scrollbars. However these are settings specific for more general UI Manipulation, head over to [The UI Configuration](UIConfiguration.md).

<img width="822" height="505" alt="image" src="https://github.com/user-attachments/assets/e93395db-3aa8-41e2-b27d-c2d6a294635f" /><br>
The image above represents the Settings Menu configs of UI for Rose of Sharon (RS)  
Here is a breakdown of all properties in a sorted table.  
| Config Property | Value Type | Explanation |
| :---: | :---: | :---: |
| BoolTrueToggleColor | TopBottomColor3 | Defines 2 colors with `Top` at the top of the circular toggle and `Bottom` at the bottom of the circular toggle when its on. **This applies to all boolean setting switches.**<br><img width="261" height="222" alt="image" src="https://github.com/user-attachments/assets/b570fe00-60f5-4af7-ad04-afaa20a8bf06" /><br>e.g. All **turned on** toggles are defined as `Top = Color3.new(0.733333, 1, 0)` and `Bottom = Color3.new(0.0431373, 0.894118, 0)` |
| BoolFalseToggleColor | TopBottomColor3 | Defines 2 colors with `Top` at the top of the circular toggle and `Bottom` at the bottom of the circular toggle when its off. **This applies to all boolean setting switches.**<br><img width="277" height="215" alt="image" src="https://github.com/user-attachments/assets/68693d9e-a514-4afd-a7a4-36c8a317551c" /><br>e.g. All **turned off** toggles are defined as `Top = Color3.new(1, 0, 0.517647)` and `Bottom = Color3.new(0.807843, 0, 0.2)` |
| SwitchablesGradient | [Gradient](Gradient.md) | Sets the [Color Gradient](Gradient.md) for all **Switchable buttons**<br><img width="243" height="281" alt="image" src="https://github.com/user-attachments/assets/85772fb1-cbbc-41c3-91ce-c01bb08b242a" /><br>e.g. this button has `SwitchablesGradient = {Color = ColorSequence.new(Color3.new(0.984314, 1, 0), Color3.new(0.956863, 0, 0.572549)), Rotation = 92, Offset = Vector2.zero}` <br>**PLEASE REFER TO [GRADIENTS](Gradient.md) TO GET A BETTER CONTEXT** |
| SwitchablesTextColor | Color3 | Sets the `Color3` of the text inside all **Switchable buttons**<br><img width="542" height="92" alt="image" src="https://github.com/user-attachments/assets/f4694088-6193-4074-8882-e071310355cf" /><br>e.g. This button text **("Day")** inside has ```SwitchablesTextColor = Color3.new(1,1,1)``` |
| ScrollerGradient | [Gradient](Gradient.md) | Sets the [Color Gradient](Gradient.md) for all **Scrolling buttons**<br><img width="48" height="175" alt="image" src="https://github.com/user-attachments/assets/287957bc-ce1f-4f70-9e63-f26d030a5a35" /><br>e.g. this scrolling button has `ScrollerGradient = {Color = ColorSequence.new({ColorSequenceKeypoint.new(0, Color3.new(1, 0.192157, 0.85098)), ColorSequenceKeypoint.new(0.5, Color3.new(1, 0.192157, 0.85098)), ColorSequenceKeypoint.new(1, Color3.new(1, 0.160784, 0.482353))}), Rotation = 90, Offset = Vector2.zero}` <br>**PLEASE REFER TO [GRADIENTS](Gradient.md) TO GET A BETTER CONTEXT** |
| RoamColor | Color3 | Sets the `Color3` of the scrollbar roam element.<br><img width="464" height="48" alt="image" src="https://github.com/user-attachments/assets/19ff07c9-a917-4902-af89-88ba6dc8c2bd" /><br>e.g. This roam element has ```RoamColor = Color3.new(0.254902, 0, 0.2)``` |


### Configuration Part 4 (Misconceptions & Traps)  
One common mistake when setting up tips is **HTML formatting** and the `SanitizeHtmlTags` property. When `SanitizeHtmlTags = false`, typing literals characters like `&`, `>`, `<`, `"` and `'` into the string field of a `{Color3.new(1, 0.360784, 0.745098),"<3 <3 <3 meow :3 omgg kawaii >~< 'o' ",},` will cause the text output to look like this

<img width="417" height="61" alt="image" src="https://github.com/user-attachments/assets/50984cb7-05c3-4daf-b589-6645c972b182" />

So for most cases it is best to leave `SanitizeHtmlTags = true` but if you want to use these characters like `&`, `>`, `<`, `"` and `'` while `SanitizeHtmlTags = false` you will need to instead type `&amp;` for `&`, `&lt;` for `<`, `&gt;` for `>`, `&quot;` for `"` and `&apos;` for `'`. If we do this for our `{Color3.new(1, 0.360784, 0.745098),"&lt;3 &lt;3 &lt;3 meow :3 omgg kawaii &gt;~&lt; &apos;o&apos; ",},` we get this result instead

<img width="425" height="36" alt="image" src="https://github.com/user-attachments/assets/0fb9c137-1add-4195-a819-362231be9ba7" />

However if we leave `SanitizeHtmlTags = true` instead you will just get the literal characters like this

<img width="418" height="60" alt="image" src="https://github.com/user-attachments/assets/846097b3-ae20-4dd1-b69c-66db737f0de7" />

Also for more information on **RichText markup** you can review the [official Roblox Documentation](https://create.roblox.com/docs/ui/rich-text) here ^0^


Another common misconception is the `AllowSprintingToggle` property, Most people would assume if this is set to `false` then sprinting will no longer be possible. This is false because all this toggle does is **Determine if you want the ability to sprint as a literal settings option to be available**


Also for about Gradients, You can review [Gradients](Gradient.md) or understand what a [ColorSequence](ColorSequence.md) is or Understand what a [Vector2](Vectors23.md) does under `Offset = Vector2.zero`


# Section 4 - Environment <3

> Before we begin, your ReplicatedStorage folder should atleast contain ```RoseOfSharonConfig```.  
> <img width="189" height="140" alt="image" src="https://github.com/user-attachments/assets/e88355e9-d1c3-44c8-935c-35681e36d3d1" /><br>
> And inside that ModuleScript it should look like this.<br>
> <img width="372" height="252" alt="image" src="https://github.com/user-attachments/assets/66593d54-54a9-4e1d-8656-8398d68052bc" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.


# Section 5 - Text Chat <3

> Before we begin, your ReplicatedStorage folder should atleast contain ```RoseOfSharonConfig```.  
> <img width="189" height="140" alt="image" src="https://github.com/user-attachments/assets/e88355e9-d1c3-44c8-935c-35681e36d3d1" /><br>
> And inside that ModuleScript it should look like this.<br>
> <img width="372" height="252" alt="image" src="https://github.com/user-attachments/assets/66593d54-54a9-4e1d-8656-8398d68052bc" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.
