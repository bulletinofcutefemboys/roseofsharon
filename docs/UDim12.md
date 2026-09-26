# Whats a UDim?<br>
A UDim in roblox is a data object used to describe **UI Objects** and specifically for ```UICorner Objects```.<br>
They contain a **scale value** and a **offset value**. Heres how UDim constructor is made.

> Suppose I have a scale of 25% and a 10 pixel offset

> Heres how I would build the constructor
```lua
local x = UDim.new(0.25 ,10)

local scale = x.Scale

local offset = x.Offset
```
| Scale | Offset |
| :---: | :---: |
| The Scale factor which determines how much percentage the **GUI object** should cover the entire screen/container (It can sometimes exceed 1) | The Offset factor white determines how much pixels it should cover. So devices with lower screen resolutions, the **GUI object** appears bigger |
| <img width="347" height="347" alt="image" src="https://github.com/user-attachments/assets/700e7c6d-81f6-47d5-9272-b7d9d4686c3e" /><br>e.g. This uses ```UDim.new(0.5,0)```, 50% radius of the UI. | <img width="347" height="347" alt="image" src="https://github.com/user-attachments/assets/bfabebcb-dd0d-460c-b488-9bfaddf48c53" /><br>e.g. This uses ```UDim.new(0,100)```, 100 pixel radius. |


# Whats a UDim2 and Examples
A UDim2 is simply **2 UDim objects combined** to define all sizes and positions of all UI Objects.<br>
It contains a ```x``` and ```y``` value.

> Suppose I have a UI Object with a 100px width and 50px width

> Heres how I would build the constructor

```lua
local size = UDim2.fromOffset(100, 50)
```

> Also Suppose I have an another UI Object with a 50% width and 25% height

> Heres how I would build the constructor

```lua
local size = UDim2.fromScale(0.5, 0.25)
```

> Now lets say i want to combine **offset and scale** with a 100px width and 50px height combined with 50% width and 25% height.

> Heres how I would build the constructor

```lua
local size = UDim2.new(0.5, 100, 0.25, 50)
```

| Offset Only | Scale Only | Offset+Scale |
| :---: | :---: | :---: |
| <img width="880" height="330" alt="image" src="https://github.com/user-attachments/assets/0818a33e-c94f-49a6-a9c1-edce487641cb" /><br>with the `UDim2.fromOffset(100, 50)` constructor. | <img width="888" height="330" alt="image" src="https://github.com/user-attachments/assets/cd97e985-989c-4426-a68a-b2e8f05fdcae" /><br>with the `UDim2.fromScale(0.5, 0.25)` constructor. | <img width="880" height="330" alt="image" src="https://github.com/user-attachments/assets/c5fde12e-7174-41ec-9e6a-d9361f3dea88" /><br>with the `UDim2.new(0.5, 100, 0.25, 50)` constructor. |


Again this also applies to UI Object positions aswell and most of the time it is **recommended to only use scale**. Only use **offset** when you need pixel borders or more precise control in UI design.



