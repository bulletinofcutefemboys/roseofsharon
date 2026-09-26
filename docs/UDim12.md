# Whats a UDim?<br>
A UDim in roblox is a data object used to describe **UI Objects** and specifically for ```UICorner Objects```.<br>
They contain a **scale value** and a **offset value**. Heres how UDim constructor is made.

> Suppose I have a scale of 25% and a 10 pixel offset

> Heres how I would build the constructor
```lua
local x=UDim.new(0.25 ,10)

local scale=x.Scale

local offset=x.Offset
```
| Scale | Offset |
| :---: | :---: |
| The Scale factor which determines how much percentage the **GUI object** should cover the entire screen/container (It can sometimes exceed 1) | The Offset factor white determines how much pixels it should cover. So devices with lower screen resolutions, the **GUI object** appears bigger |
| <img width="347" height="347" alt="image" src="https://github.com/user-attachments/assets/700e7c6d-81f6-47d5-9272-b7d9d4686c3e" /><br>e.g. This uses ```UDim.new(0.5,0)```, 50% radius of the UI. | <img width="347" height="347" alt="image" src="https://github.com/user-attachments/assets/bfabebcb-dd0d-460c-b488-9bfaddf48c53" /><br>e.g. This uses ```UDim.new(0,100)```, 100 pixel radius. |


# Whats a UDim2 and Comparisons
A UDim2 is simply **2 UDim objects combined** to define all sizes and positions of all UI Objects.
