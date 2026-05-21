# GDIM 33 In-Class Activities
## W1
### Activity 1
[Inspiration Board](https://docs.google.com/drawings/d/1dxorjoHsMiGoPXZ-0ofgFU93JSiXNur6REXIowsvHMo/edit?usp=sharing)

1. From my inspiration board, I think some ideas I currently have for my game is that I want it to be a game of minigames similar to the WarioWare series, but with all the games or challenges being presented within a consistent world with set platforming mechanics (still not decided whether I want to do this in 2D or 3D). A lot of the games and things I've been into lately have a varitey of games and/or challenges within their medium, like with the various card games you can play with any deck of cards or with the various tasks you see contestants handle on Taskmaster. Along with this, I think I want my game to have a kind of cartoony and/or cute kind of aesthetic as it's a vibe in games that I really enjoy, with prominent examples including Chicory or Lil Gator Game.
2. I talked with Emiko, and she was talking about making a JRPG as it's a genre that she'd been into lately. In that aspect, I could connect with her interest in the genre as while I haven't played a lot of them myself, I like watching people play them and when I do play them, I end up enjoying it. We also both admitted to being bad at explaining our ideas.
3. I chatted with Elijah and although we didn't talk about games, they told me they liked the environments I put on my inspiration board and told me about a skybox in Unity that I could use that looked similar to it.


### Activity 2
[Break-Down Image](https://docs.google.com/drawings/d/1AbqQmmtKnX526lXY_CJmbZrr-NEuwEeaSj1bynbaV3U/edit?usp=sharing)


## W4
### Activity 1
1a. In my build right now, players control a player character in first person that can walk and jump around the world (camera control not yet implemented). They can pick up an item in the world, a ball, by running into it, which boosts their jump height. There are also walls in the world for players to jump over.
1b. For my playtest, my primary goal is to learn what aesthetics my players think would best go along with my game, to get a better idea of what I want to do aesthetically in my world. Other than that, I also want to ask how my speed and jump values feel currently and if they feel good to move with or need some adjusting.

2. Playtesting Team: Jeremiah Yang(Me), Brandon Tsay, Ke-Chieh Chang, Jingyi Cheng

3. Playtesting Notes:
   - Ball item sticks to player wherever they touch it from, need to fix
  
   - Ball feels rigid, players suggested making it "feel" bouncier by making it a bouncy ball or possibly balloon
  
   - Movement smooth, jump feels too floaty though
  
   - Needs camera movement as gameplay feels restricted currently

### Activity 2
1. As long as the scale of the game was practical, a writer could easily write more dialogue without having to code anything as they can just add more dialogue nodes and connect them together, which can all be done within Unity.
   
2. The only technically real limit is the # of choices you can have on screen, but in sense of practicality, at some point there probably become too many dialogue nodes to properly organize in your project files, plus I imagine that a massive number of them could slow down or add to the size of the game negatively.

3. It creates all the Nodes that are available to create based on what things you have installed in your code library.


## W5
### Activity 1
#### 1. Basic Steps
1a. Create a QuestNode ScriptableObject class.

1b. Create a class that checks for quest completion and, if complete, runs next mission by checking QuestNode class.

#### 2. Substeps
2a. Create QuestNode ScriptableObject class and create them in project to test if its working.

2b. Create a GameController script that keeps track of the current quest, adding a QuestNode member variable. Test by attatching one of your created QuestNodes in Unity to this script (To do this, create an empty object and attach the script to it).

2c. Add a method in the GameController script that checks if the QuestStatus of the QuestNode member variable is "Complete". Test by using Debug.Log to write to console when QuestStatus of current QuestNode is "Complete".

2d. Adjust the last method to set the script's QuestNode member variable to the nextQuest QuestNode variable stored in the current QuestNode. Test by using Debug.Log to send a message if the current QuestNode is different than the one initially stored in it. 

### Activity 2
Today, I got the main chunk of my quest system working. I created a ScriptableObject class (QuestNode) that keeps data about a quest, with the important information that actually affects things right now being the questStatus, an enum variable keeping track of the completion status of the quest between Ongoing, Complete, and Failed. Also, it holds a QuestNode variable, nextQuest, which should be the following quest once the player completes the current one. To get this going though, I also created a GameController script that checks for the completion status of the currentQuest, a QuestNode member variable holding the system's current quest. If the status is Complete, than the currentQuest is set to whatever the current currentQuest's nextQuest variable is set to. Testing this all in Unity, I created an empty GameController object in my scene and added the GameController script to it along with creating and then attaching some QuestNodes to test everything out. 

## W6
### Activity 1
#### Pre-Playtest
1. Nothing new has been added since milestone 1 :|.
2. [Playtesting Link](https://1234321blue.itch.io/playtest-2-gdim-33)
3. My playtesting goal for today is to find out if the movement and camera control in my current build feels smooth/nice to play with.
#### Playtesting Notes
1. Camera could be adjusted to possibly bounce a little to give a more realistic feel.
2. Add indicators for what ability is powered up when holding an item.
3. Add indicators for where the objective of any given mission.
### Activity 2
1. By multiplying color vectors RGB with the values being decimals on a scale of 0 to 1, meaning the values are likely less than 1, the resulting vector will have values closer to 0, which ultimately make the colors closer to black, meaning they get blacker and less saturated.
2. Multiplying Alpha values together will make the resulting value more transluscent as multiplying decimals less than one together result in a smaller value, or more specifically in this case a value closer to 0, which makes the value more transluscent.
3. The vertexes on the shiba model holds the UV values that match up to the shiba texture we have.
4. Manipulating colors with math sounds terrifying and confusing to me. I haven't done actual math in a hot minute, so I don't know how well I can take use or even understand it. Plus, it's mean to take the simplicity of color we learned as children and adding bad, bad, evil numbers to it.

## W7
1. The data for the Vertex Color Node came from the shiba mesh itself.
2. The blending of colors in the shiba from step 3 results from the interlopation of data from the vertices, filling all the spaces in between all the verticies. This means that as the surface normals begin adjusting on the surface of the shiba and the vectors in turn start to change colors, the space between the verticies would form a more gradual color shift as they get closer or farther from a vertex point. 
3. The shiba we rendered with a texture is more detailed than the one we rendered with a vertex color as there is more variance in the color of verticies with the texture than the one rendered with the vertex color, meaning more aspects of the shiba pop out than the one today which was fairly similar colors in similar regions.
4. For the shiba in step 3, there is a green splotch randomly on its left thigh amongst the shades of blue, indicating possibly something wrong with the surface normals there.
5. You could possibly test UV Maps with the same type of color output testing so you could visualize where your texture would go on your mesh once you learned what the color association of a texture to a mesh was. 
6. As observed in question 4, the back of the shiba has some vertices with weird surface normals, resulting in a different dot products than of the vertices around that area, thereby creating a weird black spot that shouldn't be there.
7. We set the Blend Mode to Addititive for the fire effect as we wanted to add the colors of the fire to the alpha value to create a colorful, transparent tint over the game object.

## W8
### Activity 1
#### Pre-Playtest
1. Nothing new has been added since milestone 2 :|.
2. [Playtesting Link](https://1234321blue.itch.io/playtest-2-gdim-33)
3. My playtesting goal for today is to find out what gameplay mechanics may be unclear in my game's current form.
#### Playtesting Notes
1. Game direction feels unclear with all the base or default assets, try and incorporate assets into scene to make for more visually interesting game with better direction.
### Activty 2C
1. fjkdal
2. At 0.5, the screen has a slight overlay of the texture, but only barely, with the original screen without the texture still appearing to be more predominant. At 0, the screen no longer has any hint of the texture over it, just being the original screen without any overlay. At 1, the screen looks like it did before we added the lerp node, where it is pitch red with the textures clearly running over the original screen. 
3. The screen looks different at different lerp values because the number we were changing determines how much percentage between the values of the original screen and the texture overlay we were applying, with values closer to 0 leaving out more of the texture overlay and values closer to 1 adding more of it. 
4. In the base sin(time) graph, values range from -1 to 1. From these, we have possible negative values, which results in the weird bright effect we got when we just inputed x as sin(time). As opposed to this, in the (sin(time)+1)/2 graph, values range from 0 to 1, meaning we just go from no overlay, to the regular texture overlay without any of the negative values interupting this transition.
