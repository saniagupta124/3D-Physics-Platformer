# 3D Physics Puzzle Platformer

A Unity-based puzzle platformer where gravity manipulation unlocks new paths and challenges spatial reasoning.

## Overview
Players flip gravity to navigate platforms and collect resources, with visual feedback communicated through custom shaders.

## Technical Highlights
- **Gravity Manipulation:** Runtime Physics.gravity overrides with Rigidbody constraint management
- **Platform Mechanics:** Quaternion-based rotation
- **Visual Feedback:** Custom HLSL surface shaders with lerp-based color transitions
- **Deterministic Physics:** Consistent simulation through FixedUpdate timing

## Implementation Details
- **Engine:** Unity 2022.3.58f1
- **Language:** C#
- **Key Systems:**
  - Physics state machine for gravity transitions
  - Collision layer management for resource gating
  - Global shader parameters driven by game state
  - Resource collection tied to physics configuration

## Shader Details
The world transitions from grayscale to full color as players progress, using:
- Custom surface shader with color space interpolation
- Global shader variables updated via script
- Real-time material property blocks for performance

## Technical Challenges Solved
- Maintaining player stability during gravity shifts
- Eliminating physics jitter during platform rotation
- Shader-based state communication without UI overhead
