<img src="https://i.imgur.com/4N3PMTS.png" width="600">

A linux server scripting API for [Sub Rosa](http://subrosagame.com/).

RosaServer uses [LuaJIT](http://luajit.org/); this means there's no hit to performance while being able to create anything from moderation tools to complex custom games with easy-to-write version agnostic code.

# Getting Started

## Installing

- Build the library or download the latest [Release](https://github.com/RosaServer/RosaServer/releases).
- Your directory should contain `libluajit.so`, `librosaserver.so`, `subrosadedicated.x64`, and the `data` folder (the last two can be found with your game install).

## Running

```bash
LD_PRELOAD="$(pwd)/libluajit.so $(pwd)/librosaserver.so" ./subrosadedicated.x64
```

The server will start as normal and `main/init.lua` will be executed.

# Documentation

For complete reference on using the Lua API, go to the [wiki](https://github.com/RosaServer/RosaServer/wiki).

# Building

If you want to build RosaServer yourself and contribute, you can use Visual Studio and WSL, or use CMake on linux itself. You'll have to run `make` inside ./LuaJIT first.

---

Thanks to these open source libraries:

- [Sol3](https://github.com/ThePhD/sol2)
- [SubHook](https://github.com/Zeex/subhook)
- [cpp-httplib](https://github.com/yhirose/cpp-httplib)
- [TinyCon](https://github.com/unix-ninja/hackersandbox)
