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
