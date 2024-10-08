
# RenderForge

RenderForge is a command-line interface (CLI) tool that automates 3D rendering workflows. It allows users to run Python scripts with Blender, manage scene modifications, and generate rendered outputs, all through simple CLI commands.

## Features

- Automate 3D rendering using custom scripts.
- Modify 3D scenes programmatically.
- Track and download rendering outputs directly via the command line.

## Getting Started

### Prerequisites

Before downloading and using RenderForge, ensure you have the following installed on your machine:

1. **Blender** – [Download here](https://www.blender.org/download/), and make sure Blender is accessible via the command line (you can check this by running `blender --version`).
2. **.NET SDK** – You’ll need this to build and run RenderForge. [Download .NET SDK](https://dotnet.microsoft.com/download).
3. **Python** – Required if your Blender scripts use Python. [Download Python](https://www.python.org/downloads/).

### Installation

#### 1. Clone the Repository

Start by cloning the RenderForge project from GitHub to your local machine:

```bash
git clone https://github.com/chevp/RenderForge.git
cd RenderForge
```

#### 2. Build the Project

Once the project is cloned, navigate into the `RenderForge` directory and build the project using the .NET CLI:

```bash
dotnet build
```

#### 3. Install Dependencies

To ensure the command-line parsing works correctly, install the necessary dependencies:

```bash
dotnet add package CommandLineParser --version 2.8.0
```

## Usage

Once you have the project built, you can start using the RenderForge CLI to automate rendering tasks.

#### Render a Scene

Use the following command to render a 3D model using a Python script and save the output image:

```bash
dotnet run -- render -s /path/to/script.py -m /path/to/model.obj -o /path/to/output.png
```

- `-s, --script`: Path to the Python script that will be executed.
- `-m, --model`: Path to the 3D model to be rendered.
- `-o, --output`: Path where the rendered image will be saved.

#### Check Job Status

You can track the status of a rendering job using its job ID:

```bash
dotnet run -- status <job-id>
```

#### Download Rendered Output

Once a render job is complete, you can download the rendered result with the following command:

```bash
dotnet run -- download <job-id> -o /path/to/output.png
```

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Make your changes and commit:
   ```bash
   git commit -m "Add new feature"
   ```
4. Push your branch and open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
