# MG3
## Devlog
1. What are the default values for floats, ints, bools, and strings?

The default value for float is 0.0f.
The default value for int is 0.
The default value for bool is false.
The default value for string is null.
I tested these by adding one member variable of each type inside the Timer class. When I checked the Inspector panel, these default values automatically appeared for each variable.

2. How does the Update method get called — is your code supposed to call it in this assignment, or does it get called some other way?

I do not manually call the Update() method in my code.
Update() is a built-in Unity message. Unity automatically runs the Update function once every frame, as long as the script is enabled and attached to an active GameObject in the scene. It runs continuously during Play Mode.

3. Explain how either the KickWeapon or TimerText class use the timer. Mention the Update() method.

I will explain the TimerText class.
The TimerText script has a reference to the Timer component to track how much game time remains.
In the Start() method, we call _gameTimer.BeginTimer() to start the countdown timer at the start of the game.
Inside the Update() method (which runs every frame), we check if the timer has finished. If IsTimerFinished() returns true, we trigger the GameOver function to stop player control and show the game over text.
Also in Update(), we call _gameTimer.GetTimeLeft() every frame to fetch the remaining time and update the on-screen text display for players to see the live countdown.

## Open-Source assets
- [Cat fighter spritesheet](https://opengameart.org/content/cat-fighter-sprite-sheet)
- [Food sprites](https://rcpstd.itch.io/pixel-food-pack)