Q³
===
![Screenshot](pics/012_1_no_wire.png)

> [!WARNING]
> This fork fixes current state of the project to make it successfully build & run on modern systems. There are no plans to continue its development.

### What is Q³?
Q³ is a project using Rust language and OpenGL to create a Quake 3 like game that takes
Quake 3 and QuakeLive maps, voxelizes them, and allows groups of players to blow the shit out
of everything in a fast-paced Quake-esque first person shooter with 100% destructible environments.
However, it's an engine with some features (listed below) rather than a game.

### Which features Q³ has?
* Multithreaded OpenGL rendering
* Half-baked BSP renderer (Quake 3 and Quake Live)
  * Quake Live map rendering is... buggy
* Skeletal animation
  * Using Quake/Doom's MD5 format
* TTF renderer
* Arbitrary mesh voxelizer (for BSP maps)
  * Using Separating Axis Theorem and instance rendering
* Basic UI with drop-down console that provides in-game tweaking/debugging
  * See [Console](https://github.com/jeaye/q3/wiki/Console)
* [Documentation on a wiki](https://github.com/jeaye/q3/wiki)

### How do I get Q³ running on my system?

> [!NOTE]
> Tested only on Linux.
>
> Ensure that you have FreeType 2, Python 2.7, and GLFW3 installed.

For initial setup, run:
```bash
./configure
```
From there, you should be able to compile and run a release build with:
```bash
make && TERM=dumb ./bin/client
```
The server can be executed via:
```bash
TERM=dumb ./bin/server
```
You may also individually build server/client or specify a debug build:
```bash
make server && make client # Make either separately
make MODE=debug # Debug symbols and faster compilation
```
