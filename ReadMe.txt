Object Pooling is a good technique used widely by game developers to improve the
performance of a game. In cases where we need to instantiate and destroy a certain
object, it is better to use Object pooling. What is done here is instead of instantiating an
object onto the scene every time the player levels up we are just going to have a particle
effect object already available on the scene when the game begins to be inactive. Then
we just set it to active and set the position to wherever you want the object to be, when
you need it, instead of instantiating a new one. Then Instead of destroying the object
we just set it to inactive and put it back in the queue, so it can be used later.
Here I have used object pooling for enemy characters, health and weapon pickups and
health regeneration and level up particle effects. A Pool Manager script is attached to
an empty game object. This script takes in a list of prefab GameObjects to be pooled
along the number of each GameObject.