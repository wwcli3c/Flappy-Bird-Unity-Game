# Flappy-Bird-Unity-Game


Play it online:  
[Click here to play](https://68d46d2955e5fc6f3e6a379a--silver-hamster-2596d9.netlify.app/)

---

## Overview

This is a **Flappy Bird** style game made with **Unity 2D**.  
The bird moves and jumps when you press the **Space key**. Your goal is to avoid pipes and score points.  

The game runs fully in the browser using **WebGL**—no installation needed.

---

## Game Scripts

### 1. PipeMoveScript
- Moves pipes to the left at a set speed.  
- Deletes pipes once they go off-screen to save memory. 

transform.position += Vector3.left * moveSpeed * Time.deltaTime;
if(transform.position.x < deadZone)
    Destroy(gameObject);
    
2. BirdScript

Controls the bird using the new Unity Input System.

Press Space to flap:

if (Keyboard.current.spaceKey.wasPressedThisFrame && birdIsAlive)
{
    myRigidbody.linearVelocity = Vector2.up * flapStrength;
}


Detects collisions. When the bird hits pipes or the ground, the game ends.

3. LogicScript

Manages the game state: start, score, game over.

Updates the UI (score text, messages, etc.).
