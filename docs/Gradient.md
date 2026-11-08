# How Gradients Work And what are they??
A Gradient is simply a table structure **containing a Color, Rotation and Offset** used mainly in `Gradient` properties in UI Configs.  
The `Color` uses a `ColorSequence` constructor, `Rotation` is a simply **number** while `Offset` is a `Vector2`


> A detailed breakdown of ColorSequence can be accessed via the [ColorSequence.md](ColorSequence.md) doc >.<

> But for oversimplification, it is used to create beautiful color gradients like from **black to white.**

```lua
local BlackAndWhite = ColorSequence.new(Color3.new(0,0,0), Color3.new(1,1,1)) --ColorSequence

local Gradient = {
  Color=BlackAndWhite,
  Rotation=0,
  Offset=Vector2.zero
}
```
<img width="540" height="78" alt="image" src="https://github.com/user-attachments/assets/1ea150ce-1b89-4895-970a-f5509977f8c0" />

> Suppose we have this 540px by 78px UI bar, with a Black to White Gradient.<br>

> If we want to **rotate it by 58 degrees** we would change the `Rotation = 58` like this

```lua
local BlackAndWhite = ColorSequence.new(Color3.new(0,0,0), Color3.new(1,1,1)) --ColorSequence

local Gradient = {
  Color=BlackAndWhite,
  Rotation=58,
  Offset=Vector2.zero
}
```
<img width="526" height="88" alt="image" src="https://github.com/user-attachments/assets/c54b1ed4-dc9b-4191-a564-61eb84c747c2" />

We now have a rotated `Gradient` but
# Whats the `Offset` property?
The Offset property is a **Vector2** that can define the central point of the entire gradient. At `Vector2.zero` it stays locked in the origin and center point of any **UI Object**  

For more information on **Vector2** check out the [Vectors23](Vectors23.md) documentation :D


> So suppose we want that central point of the gradient to be at center of the right edge of the UI Frame

> Because The Vector2 judges based on percentage of the UI Objects dimensions, so 0.5 would be 50% of the way of the UI Object

> So to achieve our goal we would do, `Vector2.new(0.5,0)` which would look like this

```lua
local BlackAndWhite = ColorSequence.new(Color3.new(0,0,0), Color3.new(1,1,1)) --ColorSequence

local Gradient = {
  Color=BlackAndWhite,
  Rotation=58,
  Offset=Vector2.new(0.5,0)
}
```
<img width="539" height="90" alt="image" src="https://github.com/user-attachments/assets/1e9599df-5cf6-40ba-a6dc-93beef0fe0ab" />

Notices how the gradient shifted all the way to the right?  
Now if we did `Vector2.new(-0.5,0)` it would be shifted all the way to the left.  
And Another thing that these lengths dont have to be **confined to [-0.5,0.5]** they can also exceed!

> Suppose a scenario where i have a `Rotation = -37` and `Offset = Vector2.new(0,3)`

```lua
local BlackAndWhite = ColorSequence.new(Color3.new(0,0,0), Color3.new(1,1,1)) --ColorSequence

local Gradient = {
  Color=BlackAndWhite,
  Rotation=-37,
  Offset=Vector2.new(0,3)
}
```
<img width="540" height="91" alt="image" src="https://github.com/user-attachments/assets/c7db2a08-04c5-44b1-83e8-4c505730a408" /><br>
---

> Now Imagine same scenario but `Rotation = 37` :3

<img width="539" height="88" alt="image" src="https://github.com/user-attachments/assets/4e47a65f-c60d-45fd-a80c-923c16efdf89" />


Now lets look at various `Rotation` at **-37 to 37** in 4 different snapshots.

| Rotation | Snapshot |
| :---: | :---: |
| -37 | <img width="540" height="91" alt="image" src="https://github.com/user-attachments/assets/c7db2a08-04c5-44b1-83e8-4c505730a408" /> |
| -12 | <img width="540" height="88" alt="image" src="https://github.com/user-attachments/assets/33da7f8f-dea1-472e-9861-c0247bdf59b5" /> |
| 12 | <img width="539" height="86" alt="image" src="https://github.com/user-attachments/assets/3710b7ba-e8e6-4b1f-a504-1c19e218749f" /> |
| 37 | <img width="539" height="88" alt="image" src="https://github.com/user-attachments/assets/4e47a65f-c60d-45fd-a80c-923c16efdf89" /> |

See how they form a circular **sunrise to sunset pattern?**<br>
Thats how these `Gradients` work and they can be used to modify in config files :D

# Fast Way to generate gradients :D
Since Rose of Sharon has a way to convert native `UIGradients` found like this one, <img width="111" height="19" alt="image" src="https://github.com/user-attachments/assets/332e2dd3-b99a-4f00-9bac-a217bbe4d007" />. You can actually use one of our plugins which you can [download here](https://create.roblox.com/store/asset/75945708279553/Rose-of-Sharon-UIGradient-To-Gradient-Parser) or review [The source code](https://github.com/bulletinofcutefemboys/roseofsharon/blob/main/src/plugins/RSUIGradient2Gradient.rbxmx).

To actually use this plugin and what each of the UI actually means heres a small guide on how to easily convert <img width="111" height="19" alt="image" src="https://github.com/user-attachments/assets/332e2dd3-b99a-4f00-9bac-a217bbe4d007" /> objects into pastable code used in the RoseOfSharon config script.

<img width="793" height="391" alt="image" src="https://github.com/user-attachments/assets/90791702-275a-4f20-906a-c519853bd03f" /><br>
First of all we need to select **Any UIGradient Object** in the explorer tab. Lets say Ill choose this one below<br>
<img width="190" height="280" alt="image" src="https://github.com/user-attachments/assets/92aa9314-2b5b-48b5-9a64-0a9a7b6439cd" /><br>
And then I will click the **Choose** button so the plugin knows which one to parse into pastable code :3 Next the "Click to find me!" button is simply a convenience feature for when your workspace is too big and itll find it and select it for you in the workspace. But after we have selected our desired UIGradient, you can modify the values below here in the **properties tab** and the properties as described and explained before.<br>
<img width="569" height="85" alt="image" src="https://github.com/user-attachments/assets/984b686f-2f77-4c43-be06-e0db54cee5e8" /><br>
Once that is ready you can then finally click the **Parse UIGradient to Gradient** button and a TextBox with pastable text will appear at the bottom, based on the properties I set I should get<br>
```lua
{
	Color=ColorSequence.new(Color3.new(1, 1, 1)),
	Rotation=0,
	Offset=Vector2.zero,
},
```
In which I can then paste this as the value of any `Gradient={...},` inside the Rose Of Sharon config script.
