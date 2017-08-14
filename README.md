## C++/ImGUI Template

This template project consists of a single library, an executable that uses the library and tests for the library with the `catch` framework. `CMake` is used for the build system.

The ImGUI library is acan create a simple GUI to debug and test things which is lightweight and portable. It uses SFML and OpenGL for that. We also provide installation steps only for SFML, because OpenGL is mostly provided by any distro.

##### How to use
```bash
> git clone https://github.com/cirquit/imgui-template
> cd imgui-template
> rm .git
> cd ..
> mv imgui-template <your-project-name>
> cd <your-project-name>
> vim CMakeLists.txt 
(modify the project names)
```

##### Install SFML

The safest way would be to build it by yourself. Download SFML [here](https://github.com/SFML/SFML/releases/tag/2.4.2).

I had these dependencies, but this may differ from your system. Just google the other libraries.

```bash
> sudo apt-get install libopenal-dev libflac++-dev
```

To install, extract the SFML archive anywhere and run these commands.

```bash
> cd SFML-2.4.2
> mkdir build && cd build
> make all
> sudo make install all
```


##### Steps to build the project
```bash
> sudo apt-get install libudev-de
> sudo cp FindSFML.cmake /usr/share/cmake-3.5.0/Modules/    (change path for your cmake version)
> sudo cp FindUDev.cmake /usr/share/cmake-3.5.0/Modules/    (change path for your cmake version)
> cd imgui-template
> mkdir build && cd build && cmake ..
```

