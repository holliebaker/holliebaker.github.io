---
layout: codelab
---

## Dungeon Crawler

1. Store and print the map.

    Start by creating a 2d array to represent the map. Use characters, e.g., `.`, `#`, `G`, and `E` to represent the contents of each map location. Populate the array with `.` (empty space). Then add one `E` (exit) at a pre-defined position. Finally, print the whole map out to the terminal.

1. Add the player.

    The player needs to know where they are, so create some variables to store their position on the map. Make sure the player shows up on the printed map.
1. Movement.

    The player should be able to move in all four directions around the map, so add user input and some conditional statements to allow them to do this. This might be a good time to wrap your user input and map printing code in a loop so that the player can continue to move around the map. Test that movement works in all directions, ensuring that the player cannot stray off the edges of the map.
1. The player view.

    With the whole map visible, the game is far too easy. The player should be able to see only a a small `5 x 5` section of the map which surrounds them. Edit your map printing code to print the player veiw. Note that if the player is at the edge or corner of the map, they should be able to see walls, e.g., if they are in the top left corner, their view should be this:
    ```
    #####
    #####
    ##P..
    ##...
    ##...
   ```
    Check that the player can move around the map and that their view displays correctly.
1. The exit.

    In order to exit the dungeon, the player must locate the ext (`E`). Once they have done so, they should be able to enter a different command (edit your user input processing code) to go through the exit. By going through the ext, they win the level and exit the game loop. At this point, you might want to randomise the position of the exit to make the game more interesting.
1. Picking up items.

    The game is still rather easy, so consider adding some elements on the map that the player can pick up. E.g., add some gold (`G`) that the player can collect, or a key (`K`) to open the exit. Keep a track of what the player has collected and incorporate it into the game's lagic. E.g., in order to go through the exit, the player must have collected five pieces of gold, or the key.
1. Additions

  - Introduce some randomness: randomly generate the player's starting position, the position of the exit, and the position of the Gold pieces.
  - Make the map more interesting: right now, the map is a plain rectangle. Think about how you could make the map more interesting, either by allowing maps to be input by the user or by automatically generating them.
  - Multiplayer: add multiple players and allow them to take turns (you'll need to track position and any collected items for all players). With multiplayer, you could also implement combat, e.g., a player could attack another player that they can see, thereby decreasing their health.
  - Dungeon Bot: develop a bot which can win the game. It has the same information as the player, i.e., it can only see the `5 x 5` section of the map.
  - Multiplayer with NPCs: building on the multiplayer and dungeon bot extensions, allow the player to compete against one (or several) bots.

