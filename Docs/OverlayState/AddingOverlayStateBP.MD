# Adding new Overlay States (Blueprint):
In order to add a new Overlay State, you will need to follow the steps below:
1. First go to **AdvancedLocomotionV4/Data/Enums** directory and open **ALS_OverlayState** file there.
2. Add your desired enum(lets call it **Overlay State** from this point on) there. I will say **MyOverlayState**
3. In order to see your desired **Overlay State** working there are few things needs to be in consideration.
    * You must have your own set of animation poses. 
    * In ALSV4 in general it is one animation sequence with a time number(not frame numer. It's like **0.04**, **0.12**, etc).
    * Sometimes don't hesitate or recopy a sequence there and use it for your own depending on your needs.
4. Next go to **AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton** and open **ALS_AnimBP** Blueprint file.
5. Open **AnimGraph** and fine **OverlayLayer** there.
6. Navigate all the way to **ALS_AnimBP > OverlayLayer > Overlay State**
7. For easyness sake or in most cases just copy an existing **animation state** there and use it for your own and name it **MyOverlayState**. [In future I plan to expand on this with nitty gritty details]
8. Connect condition pins to your newly created **MyOverlayState**. In general it goes like this
    * **<--Overlay State->** to **MyOverlayState** is a condition equal to your enum **MyOverlayState**
    * **<--Overlay State->** to **MyOverlayState** is a condition not equal to your enum **MyOverlayState**
9. Replace sequence poses you need with what you want.
10. Now go to **AdvancedLocomotionV4/Blueprints/CharacterLogic** and open **ALS_AnimMan_CharacterBP**
11. Now set new/reuse old animation for following functions for your **MyOverlayState**
    * GetRollAnimation
    * GetMantleAsset
    * GetGetupAnimation
12. Additionally use **UpdateHeldObject** for your **Props**

Credit: [Ki_99](https://www.youtube.com/channel/UCUkf-cXGx9zqdZL42BELVjA) Bigbossbro08