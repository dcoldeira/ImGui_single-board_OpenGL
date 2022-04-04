# ImGui_single-board_OpenGL (on linux)

OpenGL for small single-board computers using the [Dear ImGui C++ library](https://github.com/ocornut/imgui)


Make sure you have the GCC compiler installed. 

The `glfw` library is also needed so if you haven't installed it yet:

```Bash
sudo apt-get update
```
Install the libraries 
```Bash
sudo apt-get install cmake pkg-config
sudo apt-get install mesa-utils libglu1-mesa-dev freeglut3-dev mesa-common-dev
sudo apt-get install libglew-dev libglfw3-dev libglm-dev
sudo apt-get install libao-dev libmpg123-dev
```

Now let's install it in the lib folder (or wherever you like..)

```Bash
cd /usr/local/lib/
```
Clone the repo and cd into it

```Bash
git clone https://github.com/glfw/glfw.git
cd glfw
```
Preper the installer and run

```Bash
sudo cmake .
sudo make
sudo make install
```

On linux it is definitelly way easier if you have the Qt Creators IDE installed, if so just run the CMakeLists.txt inside the Qt creators and that it! (Qt creators is not needed, but it does have all the development dependancies needed)
