![project screenshot](https://i.imgur.com/qKVKUfo.jpg)

A proof of concept for a translucency / fake subsurface-scattering shader, based on multiple passes.

This technique stores view space z-coordinates in the framebuffer's alpha channel. It performs several passes with different blend operations to mask out light from backfaces based on the difference in depth between front- and backfaces.
The shader requires HDR rendering (for a 16 bit alpha channel) and uses a total of 5 drawcalls, but it works without thickness maps, wrap lighting or reading from the depth buffer, and it can handle animated geometry.
Only tested on Windows/DirectX.

The sample project uses test models downloaded from Morgan McGuire's Computer Graphics Archive https://casual-effects.com/data
The proof of concept shader itself is MIT-licensed (license placed at the top of the shader file).

![overview](https://i.imgur.com/0cOejYS.jpg)
