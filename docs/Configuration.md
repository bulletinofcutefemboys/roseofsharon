# Table of Contents
<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/4b02dde0-bc11-4659-9413-c5134fdcd1c7" height="32" width="32"/></td>
    <td><a href="#section-1---loading-screens-3"><b>Section 1 - Loading Screens &lt;3 </b></a></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/16f48b7d-c44e-4e97-802a-5ccddd56b60e" height="32" width="32"/></td>
    <td><a href="#section-2a---wip-game-3"><b>Section 2a - WIP &lt;3</b></a></td>
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

# Section 2a - Wip Game <3

> Before we begin, your ReplicatedFirst folder should look like this.  
> <img width="411" height="58" alt="image" src="https://github.com/user-attachments/assets/9a24df2b-4238-41fe-b89d-c89b5638bbc2" />  
> If not, please review [The Installation Guide](Installation.md) and follow instruction so things dont break.

