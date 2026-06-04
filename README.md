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

Feedback: Fix canvas UI size, and change font color to be more visible. Make UI bigger, add more decoration. Clearify enemy hitbox. Add attack feedback, let enemies splash blood or something?

### Activity 2
1. Since RGB color has less light in one pixel when its value is closer to 0, Multiplying two values less than 1 will make the product smaller. Therefore, multiplying one RGB value to the other will make the output darker than the input.
2. The alpha value will be smaller, therefore more translucent than the original values. For alpha, 1 means completely visible, and 0 means invisible.
3. It gets those values from the mesh's UV coordinates.
4. It's very useful but not very exciting, because I've been using these tools for both 2D and 3D asset making.


## W7
### Devlog Questions
1. The vertex of the mesh itself.
2. The shader blends the colors of each vertext with gradient, so visually, the colors change at the edges of each polygon.
3. Vertex color information is stored per vertex instead of per pixel, so it only shows the pixel colors that are located on vertex. All other pixel color information are lost.
4. There's a patch on the shiba's butt that has lower normal than vertex surrounding it.
5. It can be used to check the xyz rotation of a mesh, so when applying materials like our fire example that uses the mesh's rotation information, the fire won't move left when it's supposed to move up.
6. The normal of that patch of vertex is buggy, pointing lower than it should.
7. Additive will only add the lighter colors to what's behind it, so visually, it's only brightening what's behind it.



## W8
### Activity 1
1. I added audio for dialogue progession and other UI interaction, and an inventory that opens and displays items for player.
2. [Itch link](https://hayaya22333.itch.io/ms3)
3. I want to playtest for the player's experience with the UI, and if they know what they're doing in the game.


Playtesting notes:
1. Decorate the ui with sprites and arts to indicate whta each was supposed to mean.
2. Remove extra dialogue from merchant after the first time
3. Make the loot drop more obvious
4. Add reload animation or something
5. Add something that'll explain what the shop items do. New ui area?
6. Add a main quest for the player, final goal?


### Activity 2C
1. The RenderPostProcessing Effects is likely associated with the effect created. That is the level that enables the red camera effect.
2. When lerp = 0, the screen looks normal, at 0.5, it's partially blended, and at 1, it's fully red from the texture.
3. The lerp node determines what percent of color the two original input is used in the final camera display. When it's at 0, the texture takes 0% effect on the final rendering, and as the lerp value grows closer to 1, the version of the original colors multiplied by texture 2d is 100% applied.
4. The new algorithm ensures that the value will always be a non-negative by making the origin located at 0.5, which is important because the lerp node can only take values from 0 to 1.


## W9
### Activity 1
Analyzing: PEAK

1. When the player's crosser hover over an item, the item shows an outline, indicating that it can be picked up. This is a post-processing effect, since other players can't see the outline activated by your crossair. I believe it's using a shader graph similar to the outline effect from week 8's in-class activity 2A. Except in this game, instead of detecting mouse hovering, it tests if the raycast from player's crosser hit the object.
2. When the player holds onto a golden BingBong statue, they become immortal, and the player model shows a rim lighting effect. This is different from the previous object outline, since the previous one expands from the sillouette, but the gradient effect in this case is on the object itself. When the player holds onto the item, the code would activate the shader, and use something related to camera normal to calculate how dark the gradient would be. This would be an object level effect, since it mess with object normals.

Feature implementation:
- Enemies get red rim lighting when they're hit by player.
- NPC outlines when you're able to talk to them, or when new dialogues are available
- Post processing like activity 2C from last week when player gets hit


### Activity 2
<img width="1691" height="978" alt="image" src="https://github.com/user-attachments/assets/f7862dc6-9f9a-44fe-bbfd-e60ef206454e" />
I made a rim lighting shader graph for enemy, as stated in activity 1. I solved it by using a normal vector and view direction node to calculate the normal between camera and mesh normal.


## W10
### Activity 1
I added grass effect, more shader graphs, and other minor fixes on player experience. I also added a quest system, new NPC that gives out quests, and a new terrain that serves the quest.

[itch.io](https://hayaya22333.itch.io/ms3)

Mainly to look for bugs, and get feedback on the visual elements of the game.

Playtesting notes: 
- Enemies should be harder: ranged/tankier/faster
- Level up after first kill
- Visual on dialogue choice

### Activity 2
1. Brainstorm the core game loop, which is basically the vertical slice.
2. Figure out the different scripts that store information for each system. When there's multiple scenes, figure how information would be communicated between these scenes.
3. For each system, construct an individual bubble diagram. Then, treat each individual system as a bubble and draw out how they effect each other.
4. For each bubble in the system, create a work breakdown that has a precise plan on how to code each listed feature. At the start or bottom, mark how informatino are passed between each bubble, like as integer, boolean, string, scriptable object... and through what action.
