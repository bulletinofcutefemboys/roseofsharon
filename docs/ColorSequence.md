# Whats a ColorSequence?
A **ColorSequence** is a roblox object in where you can create beautiful color gradients. They allow for more color control and in UI Design, they are very important. So how do they work?

A ColorSequence is actually a table of atleast 2 `ColorSequenceKeypoint` elements ranging from `t=0` to `t=1`. Here is how you would construct a `ColorSequence` Using just one color and no linear gradients
```lua
local MyPink = ColorSequence.new(Color3.new(1, 0.278431, 0.686275))
```
<img width="471" height="96" alt="image" src="https://github.com/user-attachments/assets/cfbc0d49-12f5-48aa-a33f-43667f351e5e" /><br>
But what if we want to have 2 colors one on `t=0` and `t=1`, well to do what all we have to do is add a 2nd argument to our ColorGradient like this below
```lua
local MySajaPink = ColorSequence.new(Color3.new(1, 0.278431, 0.686275), Color3.new(1, 0.0745098, 0.443137))
```
<img width="475" height="95" alt="image" src="https://github.com/user-attachments/assets/e27f5c12-5812-4cda-af07-05195277baa6" /><br>
<br>
But agaim, what if we want more than just 2 colors, what if we want a rainbow instead? Or perhaps any custom gradient >.<
Well to do that we need a `table` of `ColorSequenceKeypoints` with the first element having a `t=0` and the last element havbing a `t=1` Aswell as the elements must have a ascending order. To show you what I mean here is a Luau ColorSequence.
```lua
local MyRainbow = ColorSequence.new({
	ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 0, 0)), -- Notice how this is the first element and it has number value of 0
	ColorSequenceKeypoint.new(1/6, Color3.fromRGB(255, 255, 0)),
	ColorSequenceKeypoint.new(2/6, Color3.fromRGB(0, 255, 0)),
	ColorSequenceKeypoint.new(3/6, Color3.fromRGB(0, 255, 255)),
	ColorSequenceKeypoint.new(4/6, Color3.fromRGB(0, 0, 255)),
	ColorSequenceKeypoint.new(5/6, Color3.fromRGB(255, 0, 255)),
	ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 0, 0)), -- Notice how this is the last element and it has a number value of 1
})
```
Notice how in each `ColorSequenceKeypoint.new`, it takes in 2 values. The first one takes a `number` ranging from `t=0` to `t=1`. This determines the **"time" or "alpha"** of the Color Sequence or how much far it sits in the `ColorSequence`.<br><br>
<img width="472" height="252" alt="image" src="https://github.com/user-attachments/assets/03713ffc-f182-4f62-8fbe-6fc028487044" /><br>
The second value takes a traditional `Color3` value which at a specified `t` will be **that specific color** as defined by `local Example = Color3.new(1, 0, 0)`.<br><br>
S
