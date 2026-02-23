# DreamsFPSProject
Modular FPS system developed in Dreams using visual logic circuits.
This is the final step of an evolving personal project I did for fun. It started with an early third-person prototype and became a fully modular first-person system featuring parametrized weapons stats (with the possibility to support different archetypes such as bows, flamethrowers, lasers, and classic firearms), automatic animation blending, recoil and accuracy system.

The architecture was designed to be scalable and easily extendable, with modular components that can be enabled or disabled per weapon, and support for both first- and third-person perspectives. extend.

# Animations

## Blend Tree Simulation
The tools provided in Dreams did not support blending between different animations, which is fundamental for an FPS to feel smooth and responsive. Using the internal logic system, I managed to simulate a blend tree using timers. Thanks to this system, I was able to create extremely smooth transitions between different weapon states with no interruptions or visual artifacts.

## Shared Parametric Animations
Dreams includes a “thermometer” system that limits how many elements can be placed inside a scene. Animations, in particular, are extremely resource-heavy, so it was not feasible to create multiple animations for each weapon.

To increase the maximum number of supported weapons, I designed a framework based on shared parametric animations. The framework manages all weapon-related animations such as walk, run, recoil, and camera movement, and each one can be customized by setting different intensity parameters.

With this approach, I significantly reduced the resource cost of a single weapon. Additionally, with this system, each new weapon only needs to define keyframes for the idle, ADS, run, and stowed states, without requiring custom timelines to manage animations.

This made adding a new weapon extremely easy and scalable.

I also added the possibility to disable the automatic animation system and implement fully custom animations for specific weapons when needed.

# Mechanics

## Weapon Swap and Modular Weapon System

## Recoil and Accuracy/Weapon Spread

## Parametric Weapon Firing Module

### Custom Improved Timer

## Shooting Mode

# Mechanics

## Modular Weapon Architecture

## Parametric Weapon Firing Module
### Custom High-Precision Timer

## Weapon Swap System

## Recoil & Accuracy System

## Animation Framework
- Blend tree simulation
- Shared parametric animations

## Future Improvements
- Ammunition system
- Physics-based projectile refinement
- Extended third-person support
