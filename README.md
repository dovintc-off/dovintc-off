<div align="center">
  <img src="photo_2026-04-01_20-07-07-round-corners.png" width="150" alt="Blomager Logo">
  
  <h1 style="font-family: 'Courier New', monospace; letter-spacing: 2px; margin-top: 10px;">
    &lt;——{ Dov1ntc }——&gt;
  </h1>
  
  <p><b>EOCS</b> — Lightweight 3D Game Engine written in C#</p>

  <div>
    <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white" alt="C#">
    <img src="https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET">
    <img src="https://img.shields.io/badge/OpenTK-0078D6?style=for-the-badge&logo=opentk&logoColor=white" alt="OpenTK">
    <img src="https://img.shields.io/badge/Lua-2C2D72?style=for-the-badge&logo=lua&logoColor=white" alt="Lua">
  </div>
  
  <div style="margin-top: 10px;">
    <img src="https://img.shields.io/badge/status-in%20development-yellow?style=flat-square" alt="Status">
    <img src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" alt="License">
    <img src="https://img.shields.io/github/last-commit/dovintc-off/Engine-on-CSharp?style=flat-square&color=orange" alt="Last Commit">
  </div>

  <div style="margin-top: 20px;">
    <a href="https://github.com/dovintc-off/Engine-on-CSharp/releases">
      <img src="https://img.shields.io/badge/Download-Latest%20Release-2ea44f?style=for-the-badge&logo=github" alt="Download">
    </a>
    <a href="https://github.com/dovintc-off/Engine-on-CSharp/wiki">
      <img src="https://img.shields.io/badge/Documentation-Wiki-0078D4?style=for-the-badge&logo=readthedocs" alt="Docs">
    </a>
    <a href="https://discord.gg/P7nzsdgZ7F">
      <img src="https://img.shields.io/badge/Community-Discord-2CA5E0?style=for-the-badge&logo=discord" alt="Telegram">
    </a>
  </div>
</div>

---

## About EOCS

**EOCS** is a custom game engine designed for flexibility and performance. It supports both 3D rendering pipelines using **OpenGL** (via OpenTK) and features a modular architecture with custom configuration formats.

### Key Features
- **Hybrid Rendering**: Seamless support for both 2D sprites and 3D models.
- **Multilingual UI**: Built-in support for English (US) and Russian (RU) with dynamic switching.
- **Lua Scripting**: Extensible logic via custom C++/C# Lua modules.
- **Strict File Organization**: Inspired by Minecraft's structure (`mods`, `datapacks`) for easy content management.

---

## Project Structure

The project follows a strict modular structure to ensure scalability:

```
EOCS/
├── src/                    # Core source code directory
│   ├── TextRenderer/       # Module for 2D text rendering using OpenGL
│   │   ├── FontAtlas.cs    # Generates texture atlases from font files for efficient batching
│   │   ├── GlyphData.cs    # Stores metadata for individual characters (UV coords, advance, size)
│   │   └── TextRenderer.cs # Main class handling string drawing, positioning, and color
│   ├── ObjLoader.cs        # Parses .obj files and loads vertex/texture/normal data into buffers
│   └── SkyBox.cs           # Manages the cubemap texture and renders the surrounding environment
│
├── Assets/                 # Static resources loaded at runtime
│   ├── 3D_objects/         # Directory for 3D models (.obj, .mtl)
│   ├── fonts/              # Font files (.ttf, .otf) used by TextRender module
│   ├── shaders/            # GLSL shader programs
│   │   ├── main/           # Default shaders for basic 3D object rendering
│   │   ├── SkyBox/         # Shaders specifically for cubemap projection
│   │   └── Text/           # Shaders for signed-distance-field (SDF) or bitmap text rendering
│   └── SkyBox/             # Cubemap textures (posx, negx, posy, etc.) for the environment
│
├── Main.cs                 # Entry point for game loop logic (Update/Draw cycles)
├── Program.cs              # Application entry point (Window initialization, context creation)
└── EOCS.sln                # Visual Studio Solution file
```

## Contributing

Contributions are welcome! If you want to improve the codebase:
1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

---

<div align="center">
  <sub>Made with ❤️ by Dov1ntc</sub>
</div>
