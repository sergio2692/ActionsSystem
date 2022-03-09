# ActionsSystem (K2Node Action)

Actions system is a plugin with a k2 node that inherit from the construct objects node, it add more feature like:
public variables exposed, exposed dispatchers, and have a subsystem that handle the life of the object.
The main reason why i created this plugin is to give an easy way to have a composite pattern between uobjects.

# How it start?

The functionality is pretty easy, you need only to create a child class of UAction, and use the node RunAction to start the object.
![image](https://user-images.githubusercontent.com/13841147/152138981-f0c3e8e7-bdb0-4554-a3f8-95adebfc8d8b.png)
![action1](https://user-images.githubusercontent.com/13841147/157554573-7a0cb077-08e8-4a6e-9197-66137737b9ad.png)

How you will see the public variables and dispatchers will show up as pin in the class (inherithed from UAction) that you created.

# Main virtual Methods

![image](https://user-images.githubusercontent.com/13841147/152139448-f4b56773-b2fb-4da0-9e6c-8e4aecb83ee8.png)

Inside the object action, will be the OnExecute called on execution, OnUpdate called every tick, OnStopExecute called after the method finish.
The method Finish will destory the object.
Notice that you don't need to worrie about of who is holding the uproperty, because is handled internally and it will be destroyed only after that the finish function is called.

# Why is useful?

Because standard uobjects (like ai tasks and so on) doesn't support composition, this plugin achieve an easy way to have more granularity between uobjects. 
