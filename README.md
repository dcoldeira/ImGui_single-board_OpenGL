# [Dear ImGui C++ library](https://github.com/ocornut/imgui) for single-board with OpenGL for host development on Debian


Make sure you have the GCC compiler and OpenGL installed. 

The `glfw` library is also needed so if you haven't installed it yet:

```Bash
sudo apt-get update
```
Install the libraries (note these are for 64-bit)

```Bash
sudo apt-get install mesa-common-dev libgl1-mesa-dev libglu1-mesa-dev
```

Then instal GLFW 3
```Bash
sudo apt-get install libglfw3
sudo apt-get install libglfw3-dev
```
Additionally if you want to install [GLAD](https://github.com/Dav1dde/glad)

```Bash
git clone https://github.com/Dav1dde/glad.git
cd glad
cmake ./
make
sudo cp -a include /usr/local/
```

On linux it is definitelly way easier if you have the Qt Creators IDE installed, if so, then just run the CMakeLists.txt inside the Qt creators and that it! (Qt creators is not needed, but it does have all the development dependancies needed)
