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
> If not, please review [The Installation Guide](https://github.com/bulletinofcutefemboys/roseofsharon/blob/main/docs/Installation.md) and follow instruction so things dont break.

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
<img width="513" height="339" alt="image" src="https://github.com/user-attachments/assets/953b2801-527e-454a-860d-728d74235456" /><br>
The image above represents all possible Loading Screen **ExtraConfigs** for Rose of Sharon Extras (RSE)  
Here is a breakdown of all properties in a sorted table.  
| Config Property | Value Type | Explanation |
| :---: | :---: | :---: |
| InitialIconSize | UDim2 | mrowwwwwwwwwwww |
| VertexIconSize | UDim2 | mrowwwwwwwwwwww |
| SetInIconSize | UDim2 | mrowwwwwwwwwwww |
| IconUICornerRadii | List of **UDim** | mrowwwwwwwwwwww |
| UITextFontFace | Enum.Font | mrowwwwwwwwwwww |
| UITextFontStyle | Enum.FontStyle | mrowwwwwwwwwwww |
| UITextFontWeight | Enum.FontWeight | mrowwwwwwwwwwww |


### Configuration Part 3 (Misconceptions & Traps)
One common misconception i see is people blindly pasting **IconAssetID/SoundStartID** into the string field and then complain why the icon/sound wont play. This is because it is not a valid **SoundID or TextureID** in the eyes of roblox. To correct paste in the correct id, here are both demo videos below of how i like to paste my ids to get the correct string for the parser :D
| SoundID | TextureID |
| :---: | :---: |
| <video src="https://github.com/user-attachments/assets/22f77ee9-d0a6-43b2-8907-5b3cc538d737" controls></video> | <video src="https://github.com/user-attachments/assets/cb70d145-6349-41e9-80e0-a67eca242952" controls></video><br> |

Once you have the ```rbxassetid://1234567890``` you can paste it into the **IconAssetID/SoundStartID** fields and it will finally be fixed >~<


Another misconception is ___please dont set NumberOfParticles to 0 or any negative integer___. This will obviously break the loading screen TwT. ___and definitely dont set NumberOfParticles to a giant number like 1,346,549,200___ your pc fans will hate u<br>
And also if your configurations dont match this AND especially the **module script**<br>
<img width="229" height="180" alt="image" src="https://github.com/user-attachments/assets/e249b792-cfc6-4ad7-bfb7-36b8fd2a0aee" /><br>
<img width="513" height="339" alt="image" src="https://github.com/user-attachments/assets/953b2801-527e-454a-860d-728d74235456" /><br>
Then you may want to add the proper values back or redo instructions on [The Installation Guide](https://github.com/bulletinofcutefemboys/roseofsharon/blob/main/docs/Installation.md)

# Section 2a - Wip Game <3

> Before we begin, your ReplicatedFirst folder should look like this.  
> <img width="411" height="58" alt="image" src="https://github.com/user-attachments/assets/9a24df2b-4238-41fe-b89d-c89b5638bbc2" />  
> If not, please review [The Installation Guide](https://github.com/bulletinofcutefemboys/roseofsharon/blob/main/docs/Installation.md) and follow instruction so things dont break.

