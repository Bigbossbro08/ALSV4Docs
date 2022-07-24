# Power of using Interface in ALSV4

In ALSV4, you will see in order to call/set/getting the values of a specific class, instead of using a cast, you will see functions calling to interfaces instead. Here's a brief example how interface can benefit you.

* In ALSV4, there are 4 types of Interface Class.
    - ALS_Character_BPI (For Character/Pawn)
    - ALS_Camera_BPI (For CameraController)
    - ALS_Controller_BPI (For PlayerController)
    - ALS_Animation_BPI (For AnimGraph)

To grossly simply for understandings sake, interface in general is a class where you can have your own function without telling what it does. If a class inherits an interface then you can add your own definition. Now from outside if you want to call a function of this class via interface definition made in the class that inherited that, it'll execute that function.

Casting can be very costy to execute. So, an interface, can solve this issue by a large margin. Also offering very clean code for OOP structure. You should try to keep one interface per class to simplify your workflow by a large margin and have a very clean code.

You can have more inheritance if you want. Personally I found using one inheritance is best. So to add your new things in classes like **ALS_Base_CharacterBP/ALS_AnimMan_CharacterBP** in interface, try to use existing ALS_Character_BPI interface instead. You may try adding new ones if you know what you need. In my personal workflow I found it making things complicated for me. So I just prefer sticking with one. If you know what you are doing then having more than one is not a bad idea to go for.

Credit: Bigbossbro08