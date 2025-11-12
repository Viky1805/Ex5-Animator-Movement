# Ex5-Animator-Movement

## Aim:

To implement character movement using the Animator component in Unity and control animations based on user input.

## Algorithm:

1.Start Unity and create a new 3D project.

2.Import a character model with an Animator Controller and required animation clips (Idle, Walk, Run, Jump, etc.).

3.Create an Animator Controller and assign animation states in the Animator window.

4.Set up transition parameters (e.g., Speed, isJumping) in the Animator.

5.Attach a C# script to the character to capture player input (using Input.GetAxis() for movement).

6.Update the Animator parameters based on input to trigger transitions.

7.Use CharacterController or Rigidbody to move the character in the game world.

8.Test and adjust the transitions for smooth animation playback.

## Program:

```
using UnityEngine;
using System.Collections;
using System.Collections.Generic;
public class NewMonoBehaviourScript : MonoBehaviour
{
    public Animator animator;
    public float inputX;
    public float inputY;

    // Start is called once before the first execution of Update after the MonoBehaviour is created
    void Start()
    {
        animator = this.gameObject.GetComponent<Animator>();
    }

    // Update is called once per frame
    void Update()
    {
        inputX = Input.GetAxis("Horizontal");
        inputY = Input.GetAxis("Vertical");
        animator.SetFloat("inputX", inputX);
        animator.SetFloat("inputY", inputY);  
    }
}

```

## Output:

<img width="1919" height="1142" alt="image" src="https://github.com/user-attachments/assets/a8c1322f-d421-41e6-b133-ca99d157da3d" />

## Result:

The character movement and animation control were successfully implemented using Unity’s Animator component.
