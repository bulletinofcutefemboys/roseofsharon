- [Section I - Loading Screens <3](#section-i---loading-screens-3)

# Section I - Loading Screens <3

Before we begin, your ReplicatedFirst folder should look like this.  
<img width="411" height="58" alt="image" src="https://github.com/user-attachments/assets/9a24df2b-4238-41fe-b89d-c89b5638bbc2" />  
If not, please review [The Installation Guide](https://github.com/bulletinofcutefemboys/roseofsharon/blob/main/docs/Installation.md) and follow instruction so things dont break.

### Configuration Part 1 (Config Values)  
<img width="229" height="180" alt="image" src="https://github.com/user-attachments/assets/e249b792-cfc6-4ad7-bfb7-36b8fd2a0aee" /><br>
The image above represents all possible configs for Rose of Sharon (RS)  
Here is a breakdown of all properties in a sorted table.  
| Config Property | Value Type | Explanation |
| :---: | :---: | :---: |
| SoundStartID | SoundID | **Plays a SoundID** while the loading screen animation of the icon just begins |
| LoadingScreenEnabled | boolean | Determines whether to **begin the loading screen or disable** it entirely |
| IconAssetID | TextureID | Inserts a **TextureID to the main icon** during the loading screen animation<br><img width="150" height="150" alt="An example of the icon display on the loading screen" src="https://github.com/user-attachments/assets/f292d962-5128-49ae-ba20-0e5ecd258180" /><br>e.g. this has ```IconAssetID = "rbxassetid://73439321896937"``` |
| CreditsShown | boolean | Whether to display **Credits** on the developer console (F9)<br><img width="1121" height="135" alt="The Developer Console Credits Input" src="https://github.com/user-attachments/assets/a817353b-4ca0-4b6f-93e7-b2c759663520" /><br>e.g. this has ```CreditsShown = true``` |
| ParticlesOnIcon | boolean | Whether to display **Expanding Particle VFX** in the loading screen animation<br><img width="1393" height="793" alt="image" src="https://github.com/user-attachments/assets/ecb99d3f-1758-4224-80b1-b75c5f4b01ec" /><br>e.g. this has ```ParticlesOnIcon = true``` |
| ParticleColor | Color3 | Determines whether what **RGB Value** the expanding particles should be default is<br>```Color.fromRGB(255,255,255)``` |
| NumberOfParticles | integer | Determines **how much particles** should be rendered in the **Expanding Particle VFX.**<br><img width="1440" height="788" alt="image" src="https://github.com/user-attachments/assets/2cc50c12-b838-4433-9136-02821b6e90cc" /><br>e.g this has ```NumberOfParticles = 1``` |


<!-- Unordered List -->
- Item 1
- Item 2
  - Sub-item 2a (Indent 2 spaces)

<!-- Ordered List -->
1. First item
2. Second item

<!-- Task List -->
- [x] Completed task
- [ ] Incomplete task

**Bold Text** or __Bold Text__
*Italic Text* or _Italic Text_
***Bold and Italic***
~~Strikethrough~~
This is <sub>subscript</sub>
This is <sup>superscript</sup>



---

| Left Aligned | Center Aligned | Right Aligned |
| :---         |     :---:      |          ---: |
| Text         | More Text      | $100.00       |
