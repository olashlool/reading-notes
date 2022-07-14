# Reading 41: Unity

### What is Unity in C# ?

Unity is a 2D/3D engine and framework that gives you a system for designing game or app scenes for 2D, 2.5D and 3D.

### UNITY VERSIONS
2019 - LONG TERM SUPPORT-STABLE

2020 - TECH TESTING NEW FEATURES


- Unity is more than an engine. It also brings a growing range of integrated services to engage, retain and monetize 
audiences. Unity provides a growing range of complimentary services to help developers make games and engage, retain
and monetize audiences.

- Our Unity Ads, Unity Analytics, Unity Cloud Build and Unity Multiplayer are fully integrated with the Unity Editor to 
make creating and managing games as smooth, simple and rewarding an experience as possible.

### 2D

The most immediately noticeable feature is the 2D view mode button in the toolbar of the Scene view. 
When 2D mode is enabled, an orthographic (ie, perspective-free) view will be set; the camera looks along the Z axis 
with the Y axis increasing upwards. This allows you to visualise the scene and place 2D objects easily.

For a full list of 2D components, how to switch between 2D and 3D mode, and the different 2D and 3D Mode settings, see 2D or 3D Projects.

- #### 2D graphics
Graphic objects in 2D are known as Sprites. Sprites are essentially just standard textures but there are special techniques 
for combining and managing sprite textures for efficiency and convenience during development. Unity provides a 
built-in Sprite Editor to let you extract sprite graphics from a larger image. This allows you to edit a number of 
component images within a single texture in your image editor. You could use this, for example, to keep the arms, 
legs and body of a character as separate elements within one image.

Sprites are rendered with a Sprite Renderer component rather than the Mesh Renderer used with 3D objects. 
You can add this to a GameObject via the Components menu **(Component > Rendering > Sprite Renderer** or alternatively, 
you can just create a GameObject directly with a Sprite Renderer already attached **(menu: GameObject > 2D Object > Sprite)**.

In addition, you can use a Sprite Creator tool to make placeholder 2D images.

- #### 2D physics
Unity has a separate physics engine for handling 2D physics so as to make use of optimizations only available with 2D. 
The components correspond to the standard 3D physics components such as Rigidbody, Box Collider and Hinge Joint, 
but with “2D” appended to the name. So, sprites can be equipped with Rigidbody 2D, Box Collider 2D and Hinge Joint 2D. 
Most 2D physics components are simply “flattened” versions of the 3D equivalents (eg, Box Collider 2D is a square while 
Box Collider is a cube) but there are a few exceptions.


### Unity User Manual 2021.3 (LTS)
The Unity User Manual helps you learn how to use the Unity Editor and its associated services. You can read it from start 
to finish, or use it as a reference.
