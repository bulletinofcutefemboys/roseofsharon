# What are Vector2 Values?
A **Vector2** value is simply 2 numbers with a `x` and `y`. These vectors can define and point to **all of 2d space** including your Config values. They are basically the `(x,y)` in code.  

Each **Vector2** can be constructed from either `Vector2.new(x,y)`, `Vector2.zero`, `Vector2.one`, `Vector2.xAxis` or `Vector2.yAxis`
Here is a table below to describe each constructor.
| Method | Explanation |
| :---: | :---: |
| Vector2.new(x,y) | The usual method when you want to define **ANY** vector with `x` and `y` |
| Vector2.zero | This is the origin vector, it is defined as `Vector2.new(0,0)`. Use this as a shorthand for `(0,0)` |
| Vector2.one | This is the vector defined as `Vector2.new(1,1)`. Use this when you want `(1,1)` |
| Vector2.xAxis | This is the vector defined as `Vector2.new(1,0)`. Use this when you only want **x-axis** |
| Vector2.yAxis | This is the vector defined as `Vector2.new(0,1)`. Use this when you only want **y-axis** |

# What are Vector3 Values?
A **Vector3** is simply 3 numbers with a `x`, `y` and `z`. These 3d vectors can define point to **all of 3D space** including some of your Config values. They are the `(x,y,z)` in code.

Each **Vector3** can be constructed from either `Vector3.new(x,y,z)`, `Vector3.zero`, `Vector3.one`, `Vector3.xAxis`, `Vector3.yAxis` or `Vector3.zAxis`
Here is a table below to describe each constructor.
| Method | Explanation |
| :---: | :---: |
| Vector3.new(x,y,z) | The usual method when you want to define **ANY** vector with `x`, `y` and `z` |
| Vector3.zero | This is the origin vector, it is defined as `Vector3.new(0,0,0)`. Use this as a shorthand for `(0,0,0)` |
| Vector3.one | This is the vector defined as `Vector3.new(1,1,1)`. Use this when you want `(1,1,1)` |
| Vector3.xAxis | This is the vector defined as `Vector3.new(1,0,0)`. Use this when you only want **x-axis** |
| Vector3.yAxis | This is the vector defined as `Vector3.new(0,1,0)`. Use this when you only want **y-axis** |
| Vector3.zAxis | This is the vector defined as `Vector3.new(0,0,1)`. Use this when you only want **z-axis** |

# What can i do with Vectors (Regardless if its 2d or 3d)??
Theres alot of cool things you can do this these **Vectors** including **addition, scalar multiplication/division and Vector multiplication/division!**

### Addition with Vectors
If you have 2 valid vectors of the same dimension like `Vector2.new(2,3)` and `Vector2.new(1,-1)` you can do

```lua
print(Vector2.new(2,3) + Vector2.new(1,-1))
```

And get back `Vector2.new(3,2)` BUT **They must be 2 valid vectors of the same dimension or it will give an error**


### Scalar Multiplication/Division
Given a vector like `K = Vector3.new(3,2,1)` we can either multiply it with a number like `0.6*K` or divide it with `K/2` heres are the expected results if we perform those operations

```lua
local K = Vector3.new(3,2,1)

print(0.6*K) --Case 1

print(K/2) --Case 2
```

And get back `Vector3.new(1.8000000715255737, 1.2000000476837158, 0.6000000238418579)` for Case 1 BUT **thats because of IEEE754 precision errors and hardware limitations**

But for Case 2 we get back `Vector3.new(1.5,1,0.5)` which is a clean number >.<


### Vector Multiplication/Division
Given 2 vectors lets say `a = Vector3.new(1,2,3)` and `b = Vector3.new(3,2,1)` we can either multiply them both like `a*b` or divide them with `a/b` so here are there results

```lua
local a = Vector3.new(1,2,3)

local b = Vector3.new(3,2,1)

print(a*b) --Case 1

print(a/b) --Case 2
```

And we get back `Vector3.new(3,4,3)` for Case 1 while we get `Vector3.new(0.3333333432674408, 1, 3)` for Case 2 but again its the same **IEEE754 precision errors** so no need to worry.
