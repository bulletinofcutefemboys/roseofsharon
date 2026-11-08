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
Also another fact is that these `ColorSequenceKeypoint.new` time values **must be ascending**. So as you notice below Element 2 has a higher `t` value than Element 3's `t` value. This violates the constructor and will yield an error D:
```lua
local MyRainbow = ColorSequence.new({
	ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 0, 0)),
	ColorSequenceKeypoint.new(2/6, Color3.fromRGB(255, 255, 0)), -- t = 2 / 6
	ColorSequenceKeypoint.new(1/6, Color3.fromRGB(0, 255, 0)), -- t = 1 / 6
	ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 0, 0)),
})
```
# Other Easier Way to generate ColorSequences
If using a Luau script to generate `ColorSequence` values seems very complex to do and confusing to execute. We actually got an easier way to make `ColorSequence` using <img width="111" height="19" alt="image" src="https://github.com/user-attachments/assets/332e2dd3-b99a-4f00-9bac-a217bbe4d007" />s. To begin lets make a new `UIGradient` object in the explorer and then we navigate to the properties tab, your properties tab should look like this below<br>
<img width="567" height="161" alt="image" src="https://github.com/user-attachments/assets/c98dc533-5578-4c41-890e-628e54e24f6c" /><br>
Now click on the `Color` property once and then click on the `...` as highlighted with the red circle.<br>
<img width="570" height="37" alt="image" src="https://github.com/user-attachments/assets/61832c30-f8e8-458d-8e74-f2ac430c8020" /><br>
<img width="618" height="170" alt="image" src="https://github.com/user-attachments/assets/f69abd30-8ed0-4554-bdd1-a84d0c7d10b4" /><br>
<br>
We will see this UI pop up on studio, To actually modify colors and manipulate the gradient, lets say we want to change the green keypoint to White and then make a new keypoint at `t=0.8` and then delete a keypoint at `t=5/6`<br>

| Here is a video of me executing that sequence |
| :---: |
| <video src="https://github.com/user-attachments/assets/9a271fc0-b547-4abf-8fc3-99f41130227a" controls></video> |


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
