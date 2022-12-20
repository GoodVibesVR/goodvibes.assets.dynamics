=========================================================================================================
    ,/#####/.                                  ,.                    **.  ..                                      
  /%/.     .(%#,                              ,#(.           *###/.      .#(.                                     
 (#.               (#((##/    /#((##*   .(#((((#/.    ,*.   ,,/#(,   (#, .(#(((##(.   /#(/(#/   *#(/(#(.
 (#,             .##.   ,#/ .((.   ,#/ .((.   ,#/.     (#, .(#/**,   (#, .((,   ,#/  (#/,,,/%(  /#(*,
  /%/.     ./##* .##.   ,#(  (#,   ,#/ .(#,   *#/.      *%/ ,#/      (#, .(#*   ,#/  (#.    .       .(%(
    ./%%%%%/,/%*   *(####,    *#%##(,    *#%#(/#(.       .#%%(       ##, .##/(#%#*    ,(####/.  *(####/.
=========================================================================================================

Thank you for downloading this Avatar Dynamics package. This package contains everything you need in order 
to setup Avatar Dynamics for haptic feedback on erogenous zones on your avatar. Inside this package you will
find a set of prefabs containing the "VRC Contact Sender" or "VRC Contact Receiver" components and an animator
containing logic to get haptic feedback on spanking.

This is a free asset delivered from GoodVibes, a dynamic OSC mapping tool. Please visit https://goodvibes.gg 
for more information. If you're having issues, want to support, contribute or just want to hang out. then 
please join our Discord at https://discord.gg/R2tTCB7MNC

This package is reliant on:
- VRCSDK 3.0

This package contains:
- Orifice Contact Receiver Prefab
- Orifice Contact Sender Prefab
- Penetrator Contact Receiver Prefab
- Penetrator Contact Sender Prefab
- Boobas Contact Receiver Prefab
- Spanking Contact Receiver Prefab
- Smacking Contact Receiver Prefab
- GoodVibes Dynamic FX Animation Controller

How it works:
These prefabs are to simplify the setup of the Avatar Dynamics for VRChat so you can more easily rig up your
model to support haptic feedback using OSC. Putting these prefabs on your model and following the instructions
below will expose the following parameters for the GoodVibes client:
- GoodVibes/Booba		-> Float
- GoodVibes/Orifice		-> Float
- GoodVibes/Penetrator	-> Float
- GoodVibes/Spanked		-> Float
- GoodVibes/SpankedBool	-> Bool
- GoodVibes/Smacked		-> Float
- GoodVibes/SmackedBool	-> Bool

These parameters been pre-configured and will be triggered when you are interacting with other players on the areas 
where you place these prefabs. The float parameters are meant to control the strength value of the Lovense toys
and the bool parameters are meant to control actions on the PiShock.

How to set it up:
The instructions below will instruct you how to do the basic installation
Orifices (Pussy example):
1. Navigate to /GoodVibes/Dynamics/Prefabs in your project files
2. Drag the following 2 prefabs into your scene:
	- GoodVibes_OrificeReceiver
	- GoodVibes_OrificeSender
3. Drag the same 2 prefabs into the Hips bone in your armature (This is to avoid Scale problems)
	- GoodVibes_OrificeReceiver
	- GoodVibes_OrificeSender
4. Set the position of these to prefabs to 0, 0, 0 to have them centered on your Hips
5. Select both prefabs and drag them so the yellow Gizmo is barely visible from the vagina opening on the model
   and the the yellow Gizmo should be in the center of the blue one.
6. Repeat above 5 steps for any other orifice that you'd want haptic feedback from and to
TIP: Don't forget to add the prefab to the Ignore Transform list of any VRC Phys Bone component affecting the parent

Penetrator:
1. Navigate to /GoodVibes/Dynamics/Prefabs in your project files
2. Drag the following 2 prefabs into your scene:
	- GoodVibes_PenetratorReceiver
	- GoodVibes_PenetratorSender
3. Drag the same 2 prefabs into the penetrator object or the root bone of the penetrator armature
	- GoodVibes_PenetratorReceiver
	- GoodVibes_PenetratorSender
4. Change position of these 2 prefabs to 0, 0, 0 to have them centered on the penetrator
5. Select both prefabs and reposition if necessary. The base of the penetrator should be positioned in the center
   of the gizmos.
6. Resize the Radius property on the VRC Contact Receiver and VRC Contact Sender component until the Gizmos ends
   by the end of the penetrator.
TIP: Don't forget to add the prefab to the Ignore Transform list of any VRC Phys Bone component affecting the parent

Boobas:
1. Navigate to /GoodVibes/Dynamics/Prefabs in your project files
2. Drag the following prefab into your scene:
	- GoodVibes_BoobasReceiver
3. Drag the same prefab into the root of one of your boob bones
	- GoodVibes_BoobasReceiver
4. Change the position of the prefab to 0, 0, 0 to have it centered on the bone
5. The Gizmo should be a bit outside of the boobas in order to still trigger when PhysBones are present. See image 
   example on Github
6. Duplicate the prefab by selecting it i nthe Hierarchy view and press CTRL+D
7. Move the duplicated prefab to the opposite bone
8. Reposition prefab to the same position as the first one but opposite
TIP: Don't forget to add the prefab to the Ignore Transform list of any VRC Phys Bone component affecting the parent

Spanking and smacking receiver:
This one requires a bit more explaning. The below steps will go through setting up the spanking and smacking receivers.
The spanking and smacking receivers will activate your toys based upon velocity and are controlled from the FX layer
animator. SpankingReceiver and SmackingReceiver are two sides of the same coin. SpankingReceiver prefab is meant to
be placed on the Hips bone to allow for some proper ass spanking, while the smacking receiver can be placed wherever.
Examples could be boobas, cheek or wherever you want to be smacked! Hitting these areas at the speed of a "Rough love tap"
will during half a second boost the parameter GoodVibes/Spanked, GoodVibes/SpankedBool or GoodVibes/Smacked, 
GoodVibes/SmackedBool to maximum for a quick boost as haptic feedback.

Setting up the basics for Spanking and Smacking:
1. Download and install VRLabs Avatars 3.0 Manager from https://github.com/VRLabs/Avatars-3.0-Manager
2. Navigate to /GoodVibes/Dynamics/Controllers in your project files
3. Merge the GoodVibes Dynamics FX controller with your avatars FX controller using VRLabs Avatars 3.0 Manager tool
4. Navigate to /GoodVibes/Dynamics/Expressionparameters in your project files
5. Add the parameters from the located parameter object into the parameters of your own avatar

Setting up the SpankReceiver:
1. Navigate to /GoodVibes/Dynamics/Prefabs in your project files
2. Drag the following prefab into your scene:
	- GoodVibes_SpankReceiver
3. Drag the same prefab into the Hips bone
	- GoodVibes_SpankReceiver
4. Change the position of the prefab to 0, 0, 0 to have it centered on the bone
5. Reposition and rescale the object until the Gizmo is covering the outside of the ass
6. Repeat above steps with the GoodVibes_SmackingReceiver with whereever you want to be smacked
TIP: Don't forget to add the prefab to the Ignore Transform list of any VRC Phys Bone component affecting the parent

You're now ready to vibe!

NOTE:
* The controllers are currently setup using "Write Defaults", it works just as well without it. If you're 
running into issues with your controller just disable "Write Defaults" on all the GoodVibes Dynamics Controller Layers.

Credits:
- Yuwukii (https://twitter.com/YukiLewdie) for testing this README