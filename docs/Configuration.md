# Table of Contents
<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/4b02dde0-bc11-4659-9413-c5134fdcd1c7" height="32" width="32"/></td>
    <td><a href="#section-1---loading-screens-3"><b>Section 1 - Loading Screens &lt;3 </b></a></td>
    <td><a href="#section-7---sound-effects-3"><b>Section 7 - Sound Effects &lt;3 </b></a></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/16f48b7d-c44e-4e97-802a-5ccddd56b60e" height="32" width="32"/></td>
    <td><a href="#section-2---music-system-3"><b>Section 2 - Music System &lt;3</b></a></td>
    <td><a href="#section-8---notifications-3"><b>Section 8 - Notifications &lt;3 </b></a></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/4b02dde0-bc11-4659-9413-c5134fdcd1c7" height="32" width="32"/></td>
    <td><a href="#section-3---settings-menu-3"><b>Section 3 - Settings Menu &lt;3 </b></a></td>
    <td><a href="#section-9---incentives-3"><b>Section 9 - Incentives &lt;3 </b></a></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/16f48b7d-c44e-4e97-802a-5ccddd56b60e" height="32" width="32"/></td>
    <td><a href="#section-4---environment-3"><b>Section 4 - Environment &lt;3</b></a></td>
    <td><a href="#section-10---ui-customization-3"><b>Section 10 - UI Customization &lt;3 </b></a></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/4b02dde0-bc11-4659-9413-c5134fdcd1c7" height="32" width="32"/></td>
    <td><a href="#section-5---text-chat-3"><b>Section 5 - Text Chat &lt;3 </b></a></td>
    <td><a href="#section-11---general-3"><b>Section 11 - General &lt;3 </b></a></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/16f48b7d-c44e-4e97-802a-5ccddd56b60e" height="32" width="32"/></td>
    <td><a href="#section-6---chat-tags-3"><b>Section 6 - Chat Tags &lt;3 </b></a></td>
    <td><a href="#section-12---misc-3"><b>Section 12 - Misc &lt;3 </b></a></td>
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
| Tips | List of `{Color3,string}` | A defined list of `{Color3,string},` where the `Color3` can be set to any color and `string` is the actual message (tip).<br><img width="810" height="105" alt="image" src="https://github.com/user-attachments/assets/70432289-86b9-4e27-8de0-8c37b1d3fb41" /><br>Notice how theres a comma after every `{Color3,string}`, This is so the script doesnt break. |
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
These last config properties represent the UI portion of Settings, you can modify the colors of the on/off switches, buttons or scrollbars. However these are settings specific for more general UI Manipulation, head over to [The UI Configuration](#section-10---ui-customization-3).

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
> <img width="392" height="277" alt="image" src="https://github.com/user-attachments/assets/0b85159e-284c-49ef-a723-bb4e84bce4d3" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.


### Configuration Part 1 (The Environment)  
You may have seen this scary looking table inside your **Environments Table config**, with a bunch of config values, arbitrary numbers and confusing terminology like `EnvironmentDiffuseScale` and `ExposureCompensation` or `ColorShift_Top` but what ill about to show you soon will make creating environments very fun without ever touching this big mess below
<img width="724" height="1326" alt="image" src="https://github.com/user-attachments/assets/d55e1d6f-ac0c-4097-91fb-17c8961d58b0" /><br>
So what we will do instead is use a plugin that we have made and its called **Environment To Table Parser** and we can [download here](https://create.roblox.com/store/asset/72686076950875/Rose-Of-Sharon-Environment-To-Table-Parser) or review [The source code](https://github.com/bulletinofcutefemboys/roseofsharon/blob/main/src/plugins/EnvironmentToTableParser.rbxmx). Once you have the plugin in your studio we will find a button with a **rose and this title**<br>
<img width="149" height="169" alt="image" src="https://github.com/user-attachments/assets/108dbc07-e78e-47a4-9efd-c9aee05e8ac4" /><br>

We click it and we will notice that the UI is all complex and weird, but do not worry because the `TypeEnvironment Name` field is typable and this is the name of the environment like for example, TypeEnvironment Name is set to `mroewnya (≧∇≦)` this means when we export we will get <img width="270" height="18" alt="image" src="https://github.com/user-attachments/assets/583949e5-023d-4049-b97c-27b1a62607e9" /> along side with other generated data 
<br>
<img width="795" height="398" alt="image" src="https://github.com/user-attachments/assets/03936233-cb3a-4096-9242-ddca8d72fabe" /><br>
So when we **click the Parse Environment To Table button**, what the plugin will do is read your entire Lighting configuration properties, skyboxes, objects inside the Lighting folder etc. and then convert it to a big table that can be used in the `Environments` configuration. Which means we dont even have to touch a single line :D
<br><br>
So because we are now manipulating the Lighting Environment in our studio as shown here below, If you would like to dig deep into lighting then I would [recommend this video](https://www.youtube.com/watch?v=99C5K1cdql8). So here we have our scene and then the properties to modify<br>
| Lighting Properties | The Scenary | Notes |
| :---: | :---: | :---: |
| <img width="170" height="163" alt="image" src="https://github.com/user-attachments/assets/48c69505-9757-4cee-830f-41c7bb387e74" /> | <img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/16cfa7e8-2a0a-4162-acd3-fa7886dd038c" /> | So here is the baseline scenary with all default roblox lighting configurations. Below is the default `Lighting` properties<br><img width="421" height="221" alt="image" src="https://github.com/user-attachments/assets/09b604cc-314d-410d-952a-ff92d4d4a1f8" /><br><img width="497" height="169" alt="image" src="https://github.com/user-attachments/assets/22f9499e-6edd-4a32-8e6e-4dc24ba0e601" /> |
| `Lighting` properties only changed | <img width="611" height="589" alt="image" src="https://github.com/user-attachments/assets/3fbdbab7-b76f-40ca-9ded-16035c822192" /> | So I changed my `Ambient` and `ColorShift_Top` to **give a more lavender tint** and aswell as the `ExposureCompensation` to 0.1 so it can be slightly brighter. Heres the exact changes below<br><img width="469" height="223" alt="image" src="https://github.com/user-attachments/assets/4533f6a2-bdfe-49c7-98d5-f84a6edc7703" /><br><img width="478" height="169" alt="image" src="https://github.com/user-attachments/assets/495ef8a2-824b-4955-8c8b-4fe51bf61432" /> | 
| `Lighting` + `Atmosphere` properties changed | <img width="630" height="602" alt="image" src="https://github.com/user-attachments/assets/aff94b35-fc86-4f7f-aa92-ec0acbad71d4" /> | So I increased the `Density` of the atmosphere to `0.40` and then added a **lavender tint to** `Color` and `Decay` and then set the `Haze` to `1` so the `Color` and `Decay` can render, as having `Haze` set to 0 will not render either those properties. And then add a flourescent `Glaze` to 1 to finish it off. Heres the exact changes below<br><img width="328" height="41" alt="image" src="https://github.com/user-attachments/assets/8783ee59-d33b-4f09-8fee-063142955e55" /><br><img width="383" height="86" alt="image" src="https://github.com/user-attachments/assets/6b71d193-aab1-403c-bbd6-76fec5037d08" /> |
| `Lighting` + `Atmosphere` + `Sky` properties changed | <img width="674" height="670" alt="image" src="https://github.com/user-attachments/assets/bb872c3d-3c16-4882-bc0f-0b3c15419a50" /> | So I basically added a skybox with these ids: `SkyboxBk="rbxassetid://135641913828326", SkyboxDn="rbxassetid://127182922880146", SkyboxFt="rbxassetid://93848466797566", SkyboxLf="rbxassetid://85039161518723", SkyboxRt="rbxassetid://98037765363993", SkyboxUp="rbxassetid://85718348811159",`<br><img width="442" height="442" alt="image" src="https://github.com/user-attachments/assets/0772c8d4-26c9-4dc1-85c3-bacd16bd425c" /> |
| `SunRays` + Other properties added | <img width="1100" height="1044" alt="image" src="https://github.com/user-attachments/assets/600593f0-9710-460c-a98f-5a16db8a8853" /> | Configured the `Intensity` property to `0.073` and then the `Spread` to `0.65` which gives it a more realistic sun ray like effect u see irl :3 <br><img width="361" height="62" alt="image" src="https://github.com/user-attachments/assets/6c83f416-2e85-41fe-81ad-430658e9e5b1" /> |
| `ColorCorrection` + Other properties added | <img width="712" height="700" alt="image" src="https://github.com/user-attachments/assets/ded12df3-b6ba-4acc-a794-e8273ba7d631" /> | Adjusted the `Saturation` by `0.2` and `Contrast` by `0.2` while creating a **very very very pale magenta** `Tint` to make daa scene pink<br><img width="375" height="106" alt="image" src="https://github.com/user-attachments/assets/e219c59b-5516-4f4a-b18e-d2835581019e" /> |
| Supplementary Blurring Effects added: `Bloom`, `UIOpeningBlur` and `DepthOfField` + other properties | <img width="715" height="699" alt="image" src="https://github.com/user-attachments/assets/347d6474-3b56-472a-8bac-61042ab584fc" /> | `Bloom` is an interesting effect because its not really a blurring effect but it has to do with the sun hitting on the parts and reflecting back, for more detail check [daa roblox documentation 4 BloomEffects](https://create.roblox.com/docs/reference/engine/classes/BloomEffect). Also here are the values I changed.<br><img width="335" height="86" alt="image" src="https://github.com/user-attachments/assets/ddeadd26-5bbf-4245-8b3b-4a56f447593e" /><br>The `DepthOfField` effect is also interesting because it is a blurring effect but it depends on your FOV, eyesight and near/far sidedness. For more info [check the roblox documentation](https://create.roblox.com/docs/reference/engine/classes/DepthOfFieldEffect). And these are the values I used for my `DepthOfField` effect<br><img width="347" height="107" alt="image" src="https://github.com/user-attachments/assets/24611f52-1c6e-4d90-8aa7-b9bf20b84ea8" /><br>And then we have the `UIOpeningBlur` which is interesting in itself because the plugin does not **RECOGNIZE** this and **YOU MUST MANUALLY SET THE SIZE AND IT MUST BE PRESENT IN THE LIGHTING OR IT WILL BREAK**<br><img width="335" height="40" alt="image" src="https://github.com/user-attachments/assets/6acd60a8-eafb-47a8-ab8e-83ffd120c847" /> |

So once we have finally configured a beautiful environment ready to export into the config module, we will finally go to the **Environment To Table Parser and click that Parse Environment To Table** button. Once we click that button we should receive a long string below with your custom environment name mine is `mroewnya (≧∇≦)` and the underlying data below. Your string should look similiar to this below.
<br>
<img width="727" height="450" alt="image" src="https://github.com/user-attachments/assets/0a02d2e3-27c0-4c9f-b34b-896c38907f32" /><br>

> Note that this string looks very small and looks liek a weird beehive shape thingy.

Afterwords we copy that string and then we make a new line by pressing the enter key and you should get something similiar to this <br>
<img width="336" height="148" alt="image" src="https://github.com/user-attachments/assets/597c389a-b92b-499e-ac1c-c1dc6af6f9a5" /><br>
And we then finally paste the string into the table and we should get this below.<br>
<img width="263" height="171" alt="image" src="https://github.com/user-attachments/assets/102b9199-26e9-47bc-ae52-b8af2061dc4b" /><br>


### Configuration Part 2 (Miscellaneous)
So below shows all of the possible settings for the Environment section of **Rose Of Sharon config**. Some of these properties like `MarkedAsNight` are interesting because it allows you to add lanterns, glowing lights and more whenever an environment is marked as **night**.
<img width="392" height="277" alt="image" src="https://github.com/user-attachments/assets/0b85159e-284c-49ef-a723-bb4e84bce4d3" /><br>
Here is a breakdown of all properties in a sorted table.  
| Config Property | Value Type | Explanation |
| :---: | :---: | :---: |
| MarkedAsNight | Map of booleans | Lists out a map of named `Environments` like **"mroewnya (≧∇≦)"** or **"（o´・ェ・｀o）"** and sets a bool value, with night being marked as `true` and day marked as `false`, A specific environment does not have to have a element inside this list if you want it to be counted as **Day**<br><img width="537" height="341" alt="image" src="https://github.com/user-attachments/assets/ec475db0-3c26-46ab-bc50-bf1a408a0a69" /><br>e.g. this lamp im standing near at, is glowing because inside the `MarkedAsNight` list I have `["（o´・ェ・｀o）"] = true,` which marks it as night and allows for objects like that lamp to illuminate. Below is a video on how you would create these illuminating objects whenever you want a lamp that only glows at **Night**.<br><video src="https://github.com/user-attachments/assets/716541af-11ff-4b2d-b8d0-348be53f8053" controls></video>Note that Quality may be garbage due to filesize compression. Also **YOU CAN USE ANY LIGHT SOURCE TYPE INCLUDING** `PointLight`, `SpotLight` or `SurfaceLight` Aslong its named exactly **"PointLight"** then itll work. |
| DefaultEnvironment | string | Selects the **default environment** when a player first joins the game.<br><img width="521" height="236" alt="image" src="https://github.com/user-attachments/assets/1e080ef3-bec7-4ace-989b-59f214c3d2ea" /><br>e.g. The default environment is set to ```DefaultEnvironment = "（o´・ェ・｀o）"``` and every new player will initially have this environment unless they change it. |
| CanPlayerChangeEnvironment | boolean | Determines if the Player can change the environment under settings.<br><img width="565" height="87" alt="image" src="https://github.com/user-attachments/assets/678084ae-89a3-4cfd-9728-13db33258e9d" /><br>e.g. The settings shows up when `CanPlayerChangeEnvironment = true` |


### Configuration Part 3 (Misconceptions)
So one thing that breaks scripts and the framework, is when you dont need a lighting effect or don't want blur especially `UIOpeningBlur` a common mistake people do is delete the object straight up. **This is incorrect practice** instead of deleting the unwanted effect, go to the properties, and check off the `Enabled` property directly or if you cannot find the `Enabled` property, set the values of that effect to `0` to effectively disable it.<br>
<img width="361" height="44" alt="image" src="https://github.com/user-attachments/assets/2f8b53f9-db93-4b2d-9fa8-655c2a453a00" />

> For Exmaple I have unchecked the `Enabled` property which disabled the eggect without breaking any scripts

And for this object called `Atmosphere` we approach it differently as shown below<br>
<img width="488" height="310" alt="image" src="https://github.com/user-attachments/assets/4a0c71fa-d5c8-492f-93fc-f2c9b95fc48a" />

> This effect does not have a `Enabled` property so instead I setted all of those arrowed values to `0`


Also One Environment value is required because if the `Environments` is empty, the script will beeak.

And also all of those Lighting Objects inside the Lighting folder **MUST BE EXACTLY AS NAMED BELOW SHOWN IN THE IMAGE** because if not, the script will break.<br>
<img width="170" height="163" alt="image" src="https://github.com/user-attachments/assets/48c69505-9757-4cee-830f-41c7bb387e74" />

# Section 5 - Text Chat <3

> Before we begin, your ReplicatedStorage folder should atleast contain ```RoseOfSharonConfig```.  
> <img width="189" height="140" alt="image" src="https://github.com/user-attachments/assets/e88355e9-d1c3-44c8-935c-35681e36d3d1" /><br>
> And inside that ModuleScript it should look like this.<br>
> <img width="681" height="628" alt="image" src="https://github.com/user-attachments/assets/c07b3ead-53ea-47fb-8354-d2e19df37e64" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.


### Configuration Part 1 (General Properties)  
<img width="344" height="127" alt="image" src="https://github.com/user-attachments/assets/1e7d55c9-000e-41c4-bb90-b50759cc2b0a" /><br>
The image above represents some Text Chat configs for Rose of Sharon (RS)  
Here is a breakdown of all properties in a sorted table.  
| Config Property | Value Type | Explanation |
| :---: | :---: | :---: |
| ChatFont | Enum.Font | Determines the master font **for the chat window and bubble chat**<br><img width="468" height="268" alt="image" src="https://github.com/user-attachments/assets/fde94eed-bee6-4112-8674-ffc38367dcc5" /><br>e.g. This chat window is using `ChatFont = Enum.Font.IndieFlower` |
| ChatFontStyle | Enum.FontStyle | Determines the master font style (Either Normal or Italicized) **for the chat window and bubble chat**<br><img width="165" height="286" alt="image" src="https://github.com/user-attachments/assets/6930df10-9d4a-4eb1-85fc-f2300411a99a" /><br>e.g. This bubble chat uses `ChatFontStyle = Enum.FontStyle.Italicized` |
| ChatFontWeight | Enum.FontWeight | Determines the master font weight **for the chat window and bubble chat**<br><img width="467" height="49" alt="image" src="https://github.com/user-attachments/assets/44ac1846-f3d6-4979-9262-4f2810189459" /><br>e.g. This chat bar is using `ChatFontWeight = Enum.FontWeight.Bold` |
| AllowRobloxDefaultColors | boolean | Sets whether if you want the default Roblox chat title colors<br><img width="152" height="62" alt="image" src="https://github.com/user-attachments/assets/f3c10b51-40df-42f9-9278-6b3ae36db22b" /><br>e.g. These people chatting currently have `AllowRobloxDefaultColors = true` |
| ChatTagOverrideDefaultColor | boolean | Sets whether if chattags should override the default chatting color set by `ChatTextColor`<br><img width="309" height="119" alt="image" src="https://github.com/user-attachments/assets/c8aed99a-5c21-4b38-a471-618a037130c1" /><br>e.g. This chat window has `ChatTagOverrideDefaultColor = false` |
| BubbleChatEnabled | boolean | Determines if Bubbles appear ontop of your avatar when you chatted something.<br><img width="207" height="344" alt="image" src="https://github.com/user-attachments/assets/682e7266-e968-44a4-a5bd-d6f62f998f9b" /><br>e.g. This bubble appeared when `BubbleChatEnabled = true`  |


### Configuration Part 2 (Bubble Chat Properties)  
<img width="622" height="274" alt="image" src="https://github.com/user-attachments/assets/68409a52-67d5-49ef-b0ac-08592dea143e" /><br>
The image above represents some Text Chat configs for Rose of Sharon (RS)  
Here is a breakdown of all properties in a sorted table.  
| Config Property | Value Type | Explanation |
| :---: | :---: | :---: |
| BubbleBackgroundColor | Color3 | Sets the bubble chat background color.<br><img width="227" height="52" alt="image" src="https://github.com/user-attachments/assets/41250459-a873-4f05-ae6d-97821404e121" /><br>e.g. This bubble chat is set to `BubbleBackgroundColor = Color3.new(0.458824, 0, 0.980392)` |
| BubbleBackgroundTransparency | number | Sets the bubble chat background transparency.<br><img width="223" height="52" alt="image" src="https://github.com/user-attachments/assets/4b003903-93e4-4845-bde6-83646ccc31f0" /><br>e.g. This bubble chat is set to `BubbleBackgroundTransparency = 0.9` |
| TailVisible | boolean | Determines if the bubble chat should have a triangular tail pointing to your avatar.<br><img width="242" height="74" alt="image" src="https://github.com/user-attachments/assets/711defef-2afc-4968-ac4c-7a0d970d4501" /><br>e.g. This bubble chat is set to `TailVisible = false` and does not have a tail |
| BubbleTextColor | Color3 | Sets the bubble chat text color.<br><img width="210" height="75" alt="image" src="https://github.com/user-attachments/assets/a004585c-4d87-4dfc-bcf1-0f3d6ccab0e6" /><br>e.g. This bubble chat text is set to `BubbleTextColor = Color3.new(0, 0.815686, 1)` |
| BubbleTextSize | integer | Sets the bubble chat text font size.<br><img width="260" height="82" alt="image" src="https://github.com/user-attachments/assets/47b01f09-9c0b-409f-a742-d36df2bda529" /><br>e.g. This bubble chat text is set to `BubbleTextSize = 48` |
| Duration | number | Sets how long each bubble chat lasts in seconds.<br><video src="https://github.com/user-attachments/assets/c129395e-adaf-4788-8b5f-1f3be0db8a03" controls></video>e.g. This bubble chat only lasts for `Duration = 3` seconds |
| VerticalTextSpacing | integer | Determines how spaced out **(in pixels)** the bubble chats should be.<br><img width="408" height="163" alt="image" src="https://github.com/user-attachments/assets/521d2013-f880-412f-ae43-7e4c4e351bec" /><br>e.g. These bubble chats are about `VerticalTextSpacing = 60` pixels apart |
| PivotOffset | [Vector3](Vector23.md) | Sets the offset (in studs) of the bubble chat stack by a [Vector3](Vector23.md) value.<br><img width="285" height="279" alt="image" src="https://github.com/user-attachments/assets/f8adb099-a3b3-4e71-88df-79566ab11da0" /><br>e.g. This bubble chat has an offset of `PivotOffset = Vector3.new(2,3,4)` |
| MaxBubbleStack | integer | Sets the max amount of bubble chats to stack up before overflowing.<br><img width="249" height="149" alt="image" src="https://github.com/user-attachments/assets/1d0ed968-35d7-4f71-8313-9291c794bff3" /><br>e.g. These bubble chats are set to `MaxBubbleStack = 3` |
| MaxVisibleDistance | number | Determines the max distance threshold (in studs) for a bubble chat stack to be seen as visible **(This does not translate to readable as this threshold only renders the text as "...")**<br><img width="72" height="78" alt="image" src="https://github.com/user-attachments/assets/fdef0e5e-7202-441b-9bd3-13a1e0920a82" /><br>e.g. This bubble chat is set to `MaxVisibleDistance = 100` and because this image above is around ~90 studs away from the bubble chat while more than `MaxReadableDistance = 40`, it shows as **...** |
| MaxReadableDistance | number | Determines the max distance threshold for a bubble chat stack to be seen and readable.<br><img width="196" height="211" alt="image" src="https://github.com/user-attachments/assets/02e19683-b4ef-4d24-894a-1dd8ab2c4b28" /><br>e.g. This bubble chat is set to `MaxReadableDistance = 40` and because this image above is around ~39 studs away from the bubble chat, it fully displays the text instead of **...** |


# Section 6 - Chat Tags <3

> Before we begin, your ReplicatedStorage folder should atleast contain ```RoseOfSharonConfig```.  
> <img width="189" height="140" alt="image" src="https://github.com/user-attachments/assets/e88355e9-d1c3-44c8-935c-35681e36d3d1" /><br>
> And inside that ModuleScript it should look like this.<br>
> <img width="372" height="252" alt="image" src="https://github.com/user-attachments/assets/66593d54-54a9-4e1d-8656-8398d68052bc" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.


# Section 7 - Sound Effects <3

> Before we begin, your ReplicatedStorage folder should atleast contain ```RoseOfSharonConfig```.  
> <img width="189" height="140" alt="image" src="https://github.com/user-attachments/assets/e88355e9-d1c3-44c8-935c-35681e36d3d1" /><br>
> And inside that ModuleScript it should look like this.<br>
> <img width="372" height="252" alt="image" src="https://github.com/user-attachments/assets/66593d54-54a9-4e1d-8656-8398d68052bc" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.


# Section 8 - Notifications <3

> Before we begin, your ReplicatedStorage folder should atleast contain ```RoseOfSharonConfig```.  
> <img width="189" height="140" alt="image" src="https://github.com/user-attachments/assets/e88355e9-d1c3-44c8-935c-35681e36d3d1" /><br>
> And inside that ModuleScript it should look like this.<br>
> <img width="372" height="252" alt="image" src="https://github.com/user-attachments/assets/66593d54-54a9-4e1d-8656-8398d68052bc" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.


# Section 9 - Incentives <3

> Before we begin, your ReplicatedStorage folder should atleast contain ```RoseOfSharonConfig```.  
> <img width="189" height="140" alt="image" src="https://github.com/user-attachments/assets/e88355e9-d1c3-44c8-935c-35681e36d3d1" /><br>
> And inside that ModuleScript it should look like this.<br>
> <img width="372" height="252" alt="image" src="https://github.com/user-attachments/assets/66593d54-54a9-4e1d-8656-8398d68052bc" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.


# Section 10 - UI Customization <3

> Before we begin, your ReplicatedStorage folder should atleast contain ```RoseOfSharonConfig```.  
> <img width="189" height="140" alt="image" src="https://github.com/user-attachments/assets/e88355e9-d1c3-44c8-935c-35681e36d3d1" /><br>
> And inside that ModuleScript it should look like this.<br>
> <img width="372" height="252" alt="image" src="https://github.com/user-attachments/assets/66593d54-54a9-4e1d-8656-8398d68052bc" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.


# Section 11 - General <3

> Before we begin, your ReplicatedStorage folder should atleast contain ```RoseOfSharonConfig```.  
> <img width="189" height="140" alt="image" src="https://github.com/user-attachments/assets/e88355e9-d1c3-44c8-935c-35681e36d3d1" /><br>
> And inside that ModuleScript it should look like this.<br>
> <img width="372" height="252" alt="image" src="https://github.com/user-attachments/assets/66593d54-54a9-4e1d-8656-8398d68052bc" /><br>
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.


# Section 12 - Misc <3
meow WIP
