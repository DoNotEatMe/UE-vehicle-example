# UE-vehicle-example

Blueprint first testcase that supposed to upload to Epic store. Initially made with 4.27 Chaos and then transferred to clean 4.27.

<details>
<summary>Initial Task</summary>
Make drivable system with follow asset for Unreal Engine 4.27 and later.  

Features to make:

1. On/off font lights;
2. Steering angle changes when driving ;
3. Back lights glowing on handbrake;
4. Customization - textures (colors), asset, steering;
5. Brake marks on handbrake;

Important to make most realistic drivable feeling as real physics.

</details>



<details> 
<summary>Time spent and task explanation</summary>
17.01 - 13:00 -> 19:20

18.01 - 9:00 -> 21:50 - 00:20

19.01 - 09:20 -> 15:00

all time spent: ~~23:30
MVP result video: https://youtu.be/pnrgo59HWJI
MVP development build: https://drive.google.com/drive/folders/14TGlnrqJo2biz9raHGHBSOPOt_atgaOp?usp=sharing

## Tasks and issues

_Partition is supposed to show mindset and progress_

**17.01**

* Tasks

Explore Asset, Import and make draft bp с chaos vehicle // 13:00 > 19:20

* Issue/Solving

Asset in blender without textures - will work with this inside engine after draft completion.

Asset without rig - using proposed blender plugin, but have issues with importing all assets in once. Not sure how it works, leaving to another time.

Trying make draft with wheels + downside -> Physics not working

**18.01**

* Tasks

Solve problem with physics// 09:00 -> 10:30

Make draft for drivable base// 10:30 -> 11:40

Build all bolid parts and texturing// 11:40 -> 12:40

Physics tuning // 12:40 -> 15:30

Brake marks // 15:30 -> 16:50

Steering angle when driving // 16:50 -> 18:10 ; 20:20 -> 21:50

Back lights on handbrake, front light, wheel jitter cosmetic fix (just turning off motion blur) // 18:30 -> 20:20

* Issue/Solving

Problem with phys contains somewhere in mesh type. If using default - gravity applied, if kinematic (as recommended everywhere) - no.

//
If you're attempting to follow this tutorial in UE4, note that when you switch your wheel simulation type to Kinematic, the vehicle will no longer fall in simulation or in game. But it will work in UE5. I don't know how the chaos vehicle plugin is supposed to work in 4.
//

In case we making asset for 4.27 and later - thinking.

4.27 chaos installed, seems all started to work near to supposed result. Continuing.
4.27 chaos correct for Phys type kinematic and wheels collision response disabeled.

Slice demonstration:
https://youtu.be/fV5QxIVeGYw

Not sure why wheels are jitter while increasing speed

Tried to realize steering angle myself, but got some problems.

Physics update, bad turn/drift on handbrake
https://youtu.be/-LA0EMRPSDM

Brake marks when wheels sleep.
https://youtu.be/sHypG6pcbaI

Realized that there is no front lights on car. Added directional light just to show result
Back lights made with emissive scale on handbrake
Wheels jitter fixed localy with console motion blur off
https://youtu.be/p5SW8E6iIhg

Steer angle additional fixes 

**18.01**

* Tasks

Tune steer, tune physics.

UI customization // 9:20 -> 10:00 ; 10:55 -> 11:50 ; 12:30 -> 14:00

UI movement hint, camera change (tps, fps) // 10:00 -> 10:50

MVP build, little cosmetics // 14:00 ->

* Issue/Solving

Motion blur fixed by console not solving shipped build issues. So, disabled motion blur in project settings. Got consult, it's common UE issue and could be solved with post process for each wheel.
</details>

<details>
<summary>Result</summary>

[Video](https://www.youtube.com/watch?v=WkBBqhItRSE) result for 4.27 Chaos


At the end transferred project to clean 4.27 without chaos vehicle system as required by Epic

[Video](https://www.youtube.com/watch?v=jDHrG5UcQeE) result for clean 4.27

</details>

