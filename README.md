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
