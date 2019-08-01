3D Tower Defence DEMO

Gameplay-video link: https://imgur.com/a/uXJfO2T
Camera self-adjustment -demo: https://imgur.com/a/JVFiIXl

Introduction:

These scripts are from a 3D tower defence demo. This demo was made as simple as possible to test if a 
game like it would be fun to play.
The game is supposed to be a casual party game, that is played with a group of people. In the game you 
try to defend your castle from enemies, with the help of various turrets. 
If the game would be developed further, different character- (tank, mage, barbarian etc.), weapon
(swords, staffs, shields, bows etc.) and enemy-types, would be added.


Features:

- System for spawning multiple types of enemies every round.
- Store for buying towers.
- Tower, that shoots projectiles at enemies (projectiles knock enemies back)
- Hub, that the enemies try to destroy.
- Modified Unity NavMesh -system, that allows enemies to aggro the player, towers and the hub.
- Two types of enemies. A minion (aggros only the hub) and a swordman (aggros the player, towers and hub).
- Player character who has a weapon, that knocks enemies back, when hit.
- Camera that adjusts itself depending on player's positions.


Scripts: (All the scripts have an "Offline"-tag, because I also tested an online version of this demo.)

AttackController
- Handles the player's ability to attack (Gets input, starts animation, checks for a collision).

Buildable
- Stores a tower's information.

BuildableController
- Handles the general damage taking of all buildables.

BuildingScripts
- Handles the player's building-functionalities like opening the building menu, buying a buildable and placing it
on the ground.

BuildingStore
- Holds the information for all of the buildables available. Has also a function for selecting a buildable.

CameraScript
- Handles the camera movement. The camera's position depends on the players' positions. 

EnemyAttackController
- Handles the enemies' attack functionalities. 

EnemyController
- Handles the enemies' navigation, aggroing and initiation of attacks. Also hold functions for the enemies to 
take damage, getting stunned and getting destroyed.

EnemySpawner
- Holds the information of each rounds wave of enemies. Also has functions for spawning the waves.

GameController
- Handles initializing the game (instantiates the players and the camera, spawns the first wave, initializes the UI
etc.). Also has functions for adding resources to the players, starting the next round and ending the game.

HubScript
- Holds the hub's information. Has functions for the hub to take damage, for initiating the end of the game, for 
opening the building-menu and closing the building-menu.

ItemManager
- Holds the information of each players items. Currently only has a field for the player's resources.

Movement
- Handles the player's movement, initiation of attacks and targeting enemies.

PlayerActionHandler
- Handles every action, that can be done to the players (getting knocked, taking damage and getting destroyed).

PlayerInfo
- Holds the player's information.

ProjectileScript
- Handles the movement of the turret's projectiles.

TurretScript
- Handles all the turrets functionalities (targeting and shooting enemies).

UI_Controller
- Holds functions for initializing and updating the UI.


My role:

This demo was completely designed and programmed by myself. I also animated the players' and enemies' attack.

What I learnt:

Quickly iterating different design ideas is a great style of working.
Became better at designing different game-systems.



