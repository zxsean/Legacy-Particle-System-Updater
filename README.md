We are releasing a tool that can be used to convert Legacy Particle Systems into new Particle System Components.

GameObjects using ParticleEmitter, ParticleAnimator, and ParticleRenderer, can use this tool to convert to using ParticleSystem and ParticleSystemRenderer Components.

Unfortunately, scripts cannot be updated automatically.

This tool is being offered because the Legacy Particle System is scheduled to be removed from Unity in the 2018 release cycle. 2018.1 begins this removal by removing all script API functionality.

To use the conversion script, simply download it and place it in your project folder inside of a folder called Editor. Next, launch the Editor, open your project, and select Assets/Upgrade Legacy Particles from the Menu. From there, you are presented with some simple options about how to proceed with the conversion.

The tool is currently a prototype - your feedback and improvements are encouraged and welcomed, in order to make it more robust. You are welcome to make modifications/fixes yourselves, and submit them to be included in the final version. We have very few example Legacy Particle Systems, and most of what we do have are contrived examples, not real world content, meaning that the tool has only had limited testing up to this point. Please use the feedback thread to let us know about any issues.

Important version Info

Due to the ongoing removal of Legacy Particles throughout recent Unity versions, the tool is not usable in all recent versions:

2017.4 and earlier: will work fully
2018.1: if your project has any scripts using Legacy Particles, they will fail to compile and the tool will be unusable.
2018.2: is the same at 2018.1
2018.3: wont work at all - Legacy Particles have been removed from this version.

Therefore, use the tool with Unity 2017.4 or older, unless you have no scripts using Legacy Particles, in which case 2018.1 and 2018.2 cannot use the tool.

Alternatively, manually fix the scripts first, and then 2018.1 and 2018.2 may use the tool.

History

1.0
Initial release
1.1
Fixed incorrect billboard mode
Added Undo support
Fixed emission using Min and Max state when Min and Max values were the same.
Fixed emission when using one shot, should be Burst.
Added support for sizeGrow.
1.2
Fixed incorrect shape when Ellipsoid emitter is (0,0,0).
Fixed emitterVelocityScale being used incorrectly. It should be inherit velocity.
Fixed velocity dampening. We need to apply this to the velocity curve.
Set duration to be max lifetime.
Fixed particles using transform scale. Legacy did not support this.
Fixed size grow. grow is not linear, we also did not handle min and max times.
1.3
Fixed compilation issues on 2017.1
Warning added for Unity version 2018.3 and newer. Legacy particles will be removed in 2018.3.
1.4
Fixed incorrect version detection and information in help message
1.5
Added compilation message for 2018.3+ to inform that this script is not supported.
