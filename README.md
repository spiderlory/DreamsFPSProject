# DreamsFPSProject
Modular FPS system developed in Dreams using visual logic circuits.
This is the final step of an evolving personal project I did for fun. It started with an early third-person prototype and became a fully modular first-person system featuring parametrized weapons stats (with the possibility to support different archetypes such as bows, flamethrowers, lasers, and classic firearms), automatic animation blending, recoil and accuracy system.

The architecture was designed to be scalable and easily extendable, with modular components that can be enabled or disabled per weapon, and support for both first- and third-person perspectives. extend.

# Animations
## Blend Tree simulation
The tools given in dreams did not account for blending between different animation, something that is fundamental for an fps to feel smooth to play. Using the internal logic, I managed to simulate a blend tree using timers. Thanks to this system I managed to create extremely fluent transitions between different weapon's states with no interruption or artifacts.
## Shared parametric animations
In the game there is a thermometer that limits how much things can be put inside a scene. Animations in particular are extremely resource heavy so it was not feasable to create multiple animations for each weapon. To increase the maximum number of weapons, I decided to create a framework with shared parametric animations. The framework manages all weapons animations related to: walk, run, recoil and camera movement and each one can be customized by setting different intensity parameters. With this approach I managed to reduce by a lot the cost of a single weapon. Not only that, with this system each new weapon only needs to set a keyframe for the idle, ads, run and stowed states without any need to create timelines to manage animations. This made adding a new gun extremely easy and scalable. I also added the possibility to disable the automatic animations and add custom animations for a specific weapon.

