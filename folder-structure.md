# Folder Structure

```
RenderForge/
│
├── RenderForgeCLI.sln                  # Solution file
├── src/
│   ├── RenderForge/
│   │   ├── RenderForge.csproj       # Project file
│   │   ├── Program.cs               # Main entry point for the CLI
│   │   ├── Converters/              # Classes for converting Blender scenes
│   │   │   ├── BlendToGltfConverter.cs # Logic to convert .blend to .gltf
│   │   │   └── BlendToJsonConverter.cs # Logic to convert .blend to level.json
│   │   ├── Exporters/               # Handles export logic for various file formats
│   │   │   └── GltfExporter.cs      # Logic to export to .gltf files
│   │   │   └── JsonExporter.cs      # Logic to export level data to .json
│   │   ├── Models/                  # Data models for level.json and .gltf
│   │   │   ├── Level.cs             # Model for level.json representation
│   │   │   └── GltfModel.cs         # Model for .gltf representation
│   │   ├── Services/                # Business logic for handling scene conversions
│   │   │   ├── SceneConversionService.cs # Service to manage .blend scene conversions
│   │   │   └── BlenderService.cs    # Service to run Blender commands for conversion
│   │   ├── Repositories/            # File handling for storing and retrieving converted files
│   │   │   └── FileRepository.cs    # Handles file I/O for .blend, .gltf, .json
│   │   ├── Utilities/               # Utility classes/helpers
│   │   │   └── CommandLineHelper.cs # Command-line argument helper functions
│   │   ├── CLI/                     # Command-line interface logic
│   │   │   └── CommandLineParser.cs # Handles command-line parsing and dispatching
│   │   └── Config/                  # Configuration files (optional)
│   │       └── AppConfig.cs         # Configuration settings (e.g., Blender executable path)
│   │
└── tests/
    ├── RenderForgeTests/
    │   ├── Services/                # Unit tests for the services
    │   │   ├── SceneConversionServiceTests.cs
    │   └── Converters/              # Unit tests for converters
    │       ├── BlendToGltfConverterTests.cs
    │       └── BlendToJsonConverterTests.cs
```
