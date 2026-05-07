# GDIM 33 In-Class Activities
## W1
### Activity 1
[Inspo Board](https://miro.com/app/board/uXjVGoFaoL8=/)
1. I'm interested in making a rpg game, about grinding and leveling up.
2. We play tft, PEAK, Cyberpunk.
3. We both play a lot of competitive games (LOL, Overwatch, Valorant, etc)

### Activity 2
<img width="783" height="590" alt="image" src="https://github.com/user-attachments/assets/a3d49875-3164-4078-bf2f-929278bbc811" />

## W2
Write your W2 Devlog here.

## W3
### Activity 1
<img width="990" height="658" alt="image" src="https://github.com/user-attachments/assets/b39163d2-9b99-469d-9bd0-a885a3d83afe" />

### Activity 2
1. We had to save that specific name because the event needs to be referenced and called in another visual script.
2. Using Debug.Log gurantees that if the log doesn't appear as expected, the bug will definitely be in the steps before. If a function was called after a step to test that step, an unexpected result could also be because of an error in the function itself.
3. Yes. One of the core mechanics is shooting, so I need to lock the cursor in game and only show a crosser in center of screen. When selling items, the cursor would be unlocked so the player can selected items for selling and buying.
4. Yes. I will also have an explore state and dialogue state. In dialogue state, enemies will not enter Aggro state.

## W4
### Activity 1
My current build contains a fps mechanic and enemy NPCs. The player can aim and shoot at NPC to deal damage, and dealing enough damage will kill the NPC and give player EXP. UI will show player level, EXP progression, and level up pop-up. The enemy will switch state to Aggro upon taking damage, and breifly flinch every time taking shot from player. Enemy also contain weak points and shields that will amplify or decrease player damage dealt. 


My play testing goal is to see if the gameplay feels smooth and reasonable, and whether feedbacks are on time and make sense. 


Members: Han Yang, Leo Abe, Jing Cheng, Tiancheng Li


Playtesting notes:
-How hitting weak points dealt more damage, which made the gameplay involve more technical skills.
-Add limitation on player power (ammo? mp?)
-Add more enemy moving scheme

### Activity 2
1. Yes. The triggers for code are already written into nodes, so the writer could insert their dialogue through the visual graph.
2. There is no limit to the number of nodes a writer can put.
3. Regenerate Nodes will compile the scriptes used to affect how nodes appear in graph. For instance, if a programmer created a new event node in script, they will have to regenerate nodes in order for it to be available as a node in the visual scripting graph. For manually added nodes that don't inherit from classes like monobehavior, so these nodes need to be added in Type Options.

## W5
### Activity 1
Step 1: Apply animation for enemy walk and idle cycle
1. Switch enemy states using state machine (already complete)
2. In each state, use On Start node to initiate looping animation
3. Use Update node to resume to the looping animation if animation is broken by stun or attack animation

Step 2: Apply animation for enemy attack
1. Write a function that returns the float distance between enemy and player in enemy script
2. Add a visual script machine on enemy
3. Starting from an update node, use the script's distance function to play attack animation when close enough to the player.
4. Add collider to enemy as hitbox, and invoke attack after playing animation, dealing damage to player if player is in hitbox.

### Activity 2
Building on the state machine built for Milestone 1, I implemented simple animation for walk and idle cycle. The resume back to animation loop from stun and attack is also implemented. I still need to make detailed model and animation in blender to replace the simple animation in unity.

## W6
### Activity 1
I added enemy attack cool down, UI for when player takes damage, ammo system with mag and reload, NPC dialogue, and UI for when the player dies.

[Itch link](https://hayaya22333.itch.io/ms2)

Playtesting Goals:
- Bugs in shooting and reloading
- Difficulty regarding enemy strength
- Does the audio and visual cues make sense
- Anything that feels missing or not fun

### Activity 2
1. Since RGB color has less light in one pixel when its value is closer to 0, Multiplying two values less than 1 will make the product smaller. Therefore, multiplying one RGB value to the other will make the output darker than the input.
2. The alpha value will be smaller, therefore more translucent than the original values. For alpha, 1 means completely visible, and 0 means invisible.
3. It gets those values from the mesh's UV coordinates.
4. It's very useful but not very exciting, because I've been using these tools for both 2D and 3D asset making. 
