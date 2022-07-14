# Reading 42: Unity

Unity is a game development platform used to build high-quality 3D/2D games that can deployed across mobile, 
desktop, VR/AR, consoles, or the web.

### Rigidbody component reference

- #### Properties
|Property:|	    Function:|
|----------|-------------|
|  Mass:  | The mass of the object (in kilograms by default).|
|  Drag   | How much air resistance affects the object when moving from forces. 0 means no air resistance, and infinity makes the object stop moving immediately.|	     
|  Angular Drag   |	How much air resistance affects the object when rotating from torque. 0 means no air resistance. Note that you cannot make the object stop rotating just by setting its Angular Drag to infinity.|	        
|  Use Gravity   |If enabled, the object is affected by gravity.|	        


- #### Details
Rigidbodies allow your GameObjects to act under control of the physics engine. This opens the gateway to behaviors such 
as realistic collisions and varied types of joints. Manipulating your GameObjects by adding forces to a Rigidbody creates 
a very different feel and look than adjusting the Transform Component directly. Generally, you shouldn’t manipulate the 
Rigidbody and the Transform of the same GameObject - only one or the other.

- #### Parenting
When an object is under physics control, it moves semi-independently of the way its transform parents move. 
If you move any parents, they will pull the Rigidbody child along with them. However, the Rigidbodies will still 
fall down due to gravity and react to collision events.

- #### Scripting
To control your Rigidbodies, you will primarily use scripts to add forces or torque. You do this by calling AddForce() 
and AddTorque() on the object’s Rigidbody. Remember that you shouldn’t be directly altering the object’s Transform when 
you are using physics.       
   
- #### Colliders
Colliders are another kind of component that must be added alongside the Rigidbody in order to allow collisions to occur. 
If two Rigidbodies bump into each other, the physics engine will not calculate a collision unless both objects also have 
a Collider attached. Collider-less Rigidbodies will simply pass through each other during physics simulation.
	    
 
- Box Collider: A cube-shaped collider component that handles collisions for GameObjects like dice and ice cubes.

- Sphere Collider : A sphere-shaped collider component that handles collisions for GameObjects like balls or other things that can be roughly approximated as a sphere for the purposes of physics

- Capsule Collider: A capsule-shaped collider component that handles collisions for GameObjects like barrels and character limbs.

- Mesh Collider : A free-form collider component which accepts a mesh reference to define its collision surface shape.

- Wheel Collider: A special collider for grounded vehicles. It has built-in collision detection, wheel physics, and a 
slip-based tire friction model. It can be used for objects other than wheels, but it is specifically designed for 
vehicles with wheels.

- Terrain Collider: A terrain-shaped collider component that handles collisions for collision surface with the same shape as the Terrain object it is attached to


## Note:

- The relative Mass of two Rigidbodies determines how they react when they collide with each other.
- Making one Rigidbody have greater Mass than another does not make it fall faster in free fall. Use Drag for that.
- A low Drag value makes an object seem heavy. A high one makes it seem light. Typical values for Drag are between .001 (solid block of metal) and 10 (feather).
- If you are directly manipulating the Transform component of your object but still want physics, attach a Rigidbody and make it Kinematic.
- If you are moving a GameObject through its Transform component but you want to receive Collision/Trigger messages, you must attach a Rigidbody to the object that is moving.
- You cannot make an object stop rotating just by setting its Angular Drag to infinity.

## Introduction to collision

Unity handles collision between GameObjects with colliders, which attach to GameObjects and define the shape of a 
GameObject for the purposes of physical collisions. A collider is invisible, and does not need to be the exact same 
shape as the GameObject’s mesh. A rough approximation of the mesh is often more efficient and indistinguishable in gameplay.

Collision is short-duration interaction between two bodies or more than two bodies simultaneously causing change in 
motion of bodies involved due to internal forces acted between them during this.
