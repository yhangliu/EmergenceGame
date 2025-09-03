Emergence By Gamertain

Members:
Aaron Lin, alin373, alin373@gatech.edu
Nathan Ng, nng49, nng49@gatech.edu
Pierre Tawadros, ptawadros3, ptawadros3@gatech.edu
Michael Babko, mbabko3, mbabko3@gatech.edu
Yang Hang Liu, yliu3803, yliu3803@gatech.edu

----------------------------------------------------

Downloaded Assets:
- Ball Package: https://assetstore.unity.com/packages/3d/props/ball-pack-446
- Egypt Package: https://assetstore.unity.com/packages/3d/environments/dungeons/egyptian-tombs-with-pyramid-69718
- Dark Ambient Music Package: https://assetstore.unity.com/packages/audio/music/dark-ambient-music-into-insanity-vol-1-freebie-284957
- Wood Texture: https://stock.adobe.com/images/grunge-wood-pattern-texture-background-wooden-planks/188935899
- Skeleton Model: https://assetstore.unity.com/packages/3d/characters/humanoids/simple-skeleton-158811
- Sarcophagus Model: https://assetstore.unity.com/packages/3d/environments/historic/ancient-sarcophagus-152292
- Player Model: https://assetstore.unity.com/packages/3d/characters/humanoids/fantasy/free-low-poly-human-rpg-character-219979
- Flashlight sound: https://www.youtube.com/watch?v=gOLB0kWxJak&pp=ygUNI-eHiOWFiemfs-aViA%3D%3D
- Player damage sound: https://www.youtube.com/watch?v=0T_NR2KY8uI&pp=0gcJCfwAo7VqN5tD
- Trap door opening sound, wall destruction sound, wrong answer sound, swinging balls sound, correct answer sound, rolling boulder sound: https://pixabay.com/sound-effects
- Inventory open, healthpack, picking up, dropping sounds: https://freesound.org/
- Button Push animation https://www.mixamo.com/#/?page=1&query=button+push
- Hardhat on player https://vrcmods.com/item/1752-HeadLight-An-Accessory-Cap-For-You-Avatar

Tutorials:
-NavMeshAgent Doors: https://www.youtube.com/watch?v=6zYPWpjpyL0
-Inverse Kinematics: https://docs.unity3d.com/Manual/InverseKinematics.html
-Unity Shader Graph: https://discussions.unity.com/t/navmeshagent-doors/909708
-Fire https://www.youtube.com/watch?v=5Mw6NpSEb2o
-Scrolling Credits: https://www.youtube.com/watch?v=cj6hwCjiVZE&ab_channel=JimmyVegas


Start Scene:
- MainMenu --> SampleScene --> Victory/GameOver

Controls:
- wasd to move body
- space to jump
- mouse movement to move camera view
- right mouse button to use flashlight
- e to pickup items and to interact with buttons
- tab access inventory
- q to drop Anubis statue

How to Play:
- Escape the dungeon while avoiding enemies and picking up Anubis statue loot
- Drop 3 Anubis statues at health stations indicated by Horus to receive a health potion
- Use your flashlight to dissolve walls hiding secret entrances (you can still pass through them, they just slow you)
- Use your flashlight to disable various enemies you come across to help you survive, refill the battery with ones you find around the map
- You score based on the Anubis statue loot you picked up if you successfully make it to the end
- Keys can be walked over to trigger the exit door to open, a sound should play indicating the door opening (every door is locked by 2 keys)

Observation Area 1 (First half of the game):
- Map is divided in two halves, the key to leave the Part 1 will be in one of the halves and requires exploration
- AI is controlled by a state machine (Patrol, Chase, Attack)
- AI will visit invisible waypoints on the map and if it sees the player in its limited vision, it will chase the player and deal damage upon being close
- Making sense of the enemy patrol patterns will help avoid getting chased
- AI will catch fire to indicate aggression
- Door will open once both keys are collected

Observation Area 2 (Second half of game after Area 1):
- Map has an exit room right ahead of the entrance
- Map has 2 puzzle rooms, the right side requires timing to get past swinging traps to acquire key 1, the left side requires puzzle questions to be answered (left to right buttons A, B, C, D) to spawn platforms for the player to jump and get close enough to acquire the key (quiz puzzle is done by a state machine)
- AI in the main room will have an observer in the center who will send mob AI to run at you
- Breaking line of sight will stop the mob from continuing so utilizing cover will help
- Observer will catch fire if it has sight of player and extinguish if it loses sight
- Shine the enemies with the flashlight consistently to kill them
- Boxes can be utilized as cover but mob movements will move the boxes, dynamically changing the environment

- Quiz answers:
- "What Yu-Gi-Oh card depicts an egyptian ankh?" (Monster reborn)
- "Who is the Egyptian God of Knowledge?" (Thoth)
- "If you have it, you want to share it. If you share it, you don't have it anymore. What is it?" (A secret)
- "The person who made it doesn't want it, the person who paid for it doesn't need it, and the person who needs it doesn't know it. What is it?" (Coffin)
- "The person who made it doesn't want it, the person who paid for it doesn't need it, and the person who needs it doesn't know it. What is it?" (coffin)
- "I can't be seen, but I can be heard. I won't answer until spoken to. What am I?" (Echo)
- "Everybody has me but I'm impossible to lose. What am I?" (A Shadow)
- "I often run, but I don't have legs. I don't need you, but you need me. What am I?" (Water)
- "What gets thrown out when it's needed, but stored away when it's not? ?" (Anchor)
- "I start off dry but emerge wet. I go in light but emerge heavy. What am I?" (Tea bag)

Game Feel
- 3D game
- Escape the tomb, if you fail to escape the enemies and traps, you die
- Victory screen and score are rewarded for completion, game over screen is given when the player fails
- Start Menu allows game start, application close, tutorial, and credits
- Ability to restart from the beginning for another run through the tomb
- Third person perspective

Precursors to fun game:
- Goal is to escape, you can collect Anubis statues to improve your score, you may need to make an effort to evade enemies and traps along the way
- There are interesting choices: Player must manage their resources carefully: keep statues to improve your score or cash out for health packs; use flashlight to improve map travel or use it to keep enemies at bay (but risk inconvenient map travel which can lead to death during the chase)
- Choices have consequences: using collectibles can restore health but being greedy for score will risk the entire playthrough, flashlight usage can help evade enemies but not using them on secret entrances risks future obstacles
- Player can engage with buttons to answer puzzles, use flashlight beams to interact with enemy AI and environment
- Decisions are not obvious
- Game is not overly difficult
- Balance flashlight battery, Anubis statue collectibles, player motion vs AI motion, player motion vs trap motion
- Reward and punishment: failure to evade enemies or pass traps will damage you, successful evasion rewards resources to restore health and equipment or keys for map progression
- Tutorial areas allow players to learn about the game
- Game introduces new challenges to work through
- Players cannot trivially beat the game without consequences


3D Character/Vehicle with real-time control:
- Player control learned from milestone
- Player control is important to gameplay (running and jumping)
- No tutorial characters
- Not a repackaged asset (skin and model are used, but never the controller)
- Player has running and jumping animations
- Dynamic controls
- Controls are intuitive
- Fluid motion
- Minimal slide and uses IK corrections when interacting with buttons
- Low latency response
- Camera is smooth
- Limited camera clipping
- No 3rd party camera
- Auditory feedback through out game interactions
- Physics simulation used


3D World with Physics and Spatial simulation:
- Physics based on milestone
- Custom environment
- Audio is associated with interactions
- Minimal Clipping
- Appropriate boundaries
- Jumping puzzle, boulders roll with physics, doors are mecanim animated with root motion, obstacles dissolve or break
- 3D movement
- Interactive environment with enemies, puzzles, and collectables
- Consistent simulation


NPC behavior and AI:
- Based on milestone
- Not repackaged assets (only used models, skins, and animation)
- Map 1 AI utilizes state behavior
- Smooth movement
- Effective and threatening enemies
- Fluid animations
- When enemies become aggressive, a violent flame bursts out of them which extinguishes when they are not a danger
- Sounds and special effects give player feedback about AI
- Difficulty is reasonable
- AI are fair
- AI in Map 2 knock over objects when approaching player

Polish:
- Start Menu exists with credit
- Pause menu will freeze game, allows restart and quitting
- Feels like an application
- No debug
- Can exit game anytime through pause menu
- No cheat mode
- GUI is styled appropriately
- Transitions between scenes
- Torches in the environment burn, traps move to present a problem
- AI will catch fire when they become angry with you, puzzles will interact with you when you are close
- Walls dissolve when you shine a flashlight at them
- Enemies will catch fire when they are aggressive, dust kicks up from player's feet
- Auditory triggers are on all interactable things
- Auditory effects on collisions
- Style is semi realistic
- Shading and lighting present
- Unified colors
- Sound theme
- Minimal glitches
- Believable barriers
- No map edges
- No stuck locations
- Stable

Fun:
- Up to grader

Problems:
- The boulder works perfectly fine in project editor but does not work when built, not sure why.
  Update: Seems to be working in build now.

Manifest (Prefabs):
- Map1 (Design Aaron) (Map Build Michael/Aaron) (Level Implementation Nathan/Aaron)
- Map2 (Design Aaron/Nathan/Hang) (Map Build Hang) (Level Implementation Nathan/Pierre)
- Tutorial (Design Hang) (Map Build Hang) (Level Implementation Hang/Michael)
- WallsTutorial (Aaron)
- Agent (Aaron / Pierre [Animation Rig])
- Flame (Aaron)
- Wall, Wall1, Wall2, Wall3 (Aaron)
- SecretEntry (Aaron)
- Dissolve (Aaron)
- NewDoor (Door and Keys set) (Aaron)
- Pause (Aaron)
- Wood (Aaron)
- Sentry (Nathan)
- Seeker (Nathan/Pierre [Animation Rig])
- Overlay (Pierre)
- Battery (Pierre)
- AnubisKey (Pierre)
- InventorySlot (Michael)
- Anubis_statue (Michael)
- Canvas prefab (for Inventory) (Michael)
- HealthPack (Michael)
- BarterPlatform (Michael)
- AnimatedPlayer (Michael/Pierre/Hang [Animation rig]/Aaron)
- MessageTrigger (Hang)
- Boulder trap (Hang)
- Lever pull (Hang)
- Platform (Hang)
- Swinging balls (Hang)
- Victory (/MainMenu/Lose) scene (Hang)
- Credits Scene (Hang)
- Loading Scenes (Hang)

Manifest (Scripts):
- AIAttack (Aaron)
- AIDetection (Aaron)
- AIController (Aaron)
- SceneChanger (Aaron/Pierre)
- ExitGame (Aaron)
- StartGameScene (Aaron)
- PauseGame (Aaron)
- NewDoorOpen (Aaron)
- KeyCollection (Aaron)
- Dissolve (Aaron)
- FlameManagement (Aaron)
- FadeObject (Aaron + Michael)
- TutorialDamage (Aaron)
- notifyplayer (Aaron)
- SlowPass (Aaron)
- seekingAI (Nathan)
- trackingAI (Nathan)
- NotifyPlayer (Pierre)
- PlayerStats (Pierre)
- TrapCollision (Pierre)
- BatteryPickup (Pierre)
- FlashLight (Pierre/Aaron)
- SkeletonAttack (Pierre)
- SkeletonAnimate (Pierre)
- Pickupitem (Michael)
- PickupItemData (Michael)
- PlayerInventory (Michael)
- PlayerMotion (Michael)
- ThirdPersonCamera (Michael)
- CameraCollisionHandler (Michael)
- BarterPlatform (Michael)
- HealthPack (Michael)
- buttonui (Hang)
- destroywalls (Hang)
- distaneCheckerBoulder (Hang)
- distanceCheckerMessage (Hang)
- leverTrigger (Hang)
- leverTriggerTutorial (Hang)
 -leverIKControl (Hang)
- quizGame (Hang)
- quizGameV2 (Hang)
- setSpeed (Hang)
- StartTutorial (Hang)
- StartCredits (Hang)
- StartMainMenu (Hang)


