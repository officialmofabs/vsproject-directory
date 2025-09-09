# Setting Up C# and ASP.NET Development Environment on Kali Linux, Windows, and macOS with .NET 9.0 and Visual Studio Code

This guide will help you set up a development environment for C# and ASP.NET Core using the latest .NET 9.0 SDK and Visual Studio Code (VS Code) on Kali Linux, Windows, and macOS.

## For Kali Linux

### Prerequisites
- Kali Linux installed on your machine.  
- Administrative privileges to install software.  
- Visual Studio Code already installed on your system.

### Step 1: Install the .NET SDK (Version 9.0)
1. Install required dependencies: `sudo apt install -y apt-transport-https`.  
2. Download and install the Microsoft package signing key: `wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb && sudo dpkg -i packages-microsoft-prod.deb`.  
3. Update the package index: `sudo apt update`.  
4. Install the .NET SDK (Version 9.0): `sudo apt install -y dotnet-sdk-9.0`.  
5. Verify the installation: `dotnet --version`. The output should display `.NET 9.x.x`.

### Step 2: Install the C# Extension in Visual Studio Code
1. Open Visual Studio Code.  
2. Open the Extensions view by clicking on the square icon in the Activity Bar or pressing `Ctrl+Shift+X`.  
3. Search for "C# Dev Kit".  
4. Click "Install" to add the extension to VS Code.

### Step 3: Create a New ASP.NET Core Project
1. Open a terminal in VS Code by selecting `Terminal` > `New Terminal` from the menu.  
2. Create a new directory for your project: `mkdir MyAspNetApp && cd MyAspNetApp`.  
3. Initialize a new ASP.NET Core web application project: `dotnet new webapp`. This command generates a basic ASP.NET Core Razor Pages web application.

### Step 4: Run the ASP.NET Core Application
1. Navigate to the project directory: `cd MyAspNetApp`.  
2. Run the application: `dotnet run`.  
3. Open your web browser and navigate to `http://localhost:5000` (or the URL provided in the output) to view your running web application.

### Step 5: Debugging in Visual Studio Code
1. Open the main Razor Pages file (e.g., `Index.cshtml` or `Program.cs`).  
2. Set a breakpoint by clicking in the gutter to the left of the line numbers where you want execution to pause.  
3. Start debugging by selecting `Run` > `Start Debugging` in the menu, or press `F5`.  
4. Use the Debug toolbar to control execution (continue, step over, step into, etc.).

## For Windows

### Prerequisites
- Windows 10 or later installed on your machine.  
- Administrative privileges to install software.  
- Visual Studio Code already installed.

### Step 1: Install the .NET SDK (Version 9.0)
1. Visit the official .NET download page: [Download .NET](https://dotnet.microsoft.com/en-us/download).  
2. Under **.NET 9.0**, select **Download .NET SDK** for Windows.  
3. Run the downloaded installer and follow the on-screen instructions.  
4. Verify the installation by opening Command Prompt or PowerShell and running: `dotnet --version`. The output should display `.NET 9.x.x`.

### Step 2: Install the C# Extension in Visual Studio Code
1. Open Visual Studio Code.  
2. Open the Extensions view by clicking on the square icon in the Activity Bar or pressing `Ctrl+Shift+X`.  
3. Search for "C# Dev Kit".  
4. Click "Install" to add the extension to VS Code.

### Step 3: Create and Run an ASP.NET Core Project
1. Open a terminal in VS Code by selecting `Terminal` > `New Terminal` from the menu.  
2. Create a new directory for your project: `mkdir MyAspNetApp && cd MyAspNetApp`.  
3. Initialize a new ASP.NET Core web application project: `dotnet new webapp`.  
4. Run the application: `dotnet run`.  
5. Open your browser and navigate to `http://localhost:5000`.

## For macOS

### Prerequisites
- macOS 11 (Big Sur) or later installed on your machine.  
- Administrative privileges to install software.  
- Visual Studio Code already installed.

### Step 1: Install the .NET SDK (Version 9.0)
1. Visit the official .NET download page: [Download .NET](https://dotnet.microsoft.com/en-us/download).  
2. Under **.NET 9.0**, select **Download .NET SDK** for macOS.  
3. Run the downloaded installer and follow the on-screen instructions.  
4. Verify the installation by opening Terminal and running: `dotnet --version`. The output should display `.NET 9.x.x`.

### Step 2: Install the C# Extension in Visual Studio Code
1. Open Visual Studio Code.  
2. Open the Extensions view by clicking on the square icon in the Activity Bar or pressing `Cmd+Shift+X`.  
3. Search for "C# Dev Kit".  
4. Click "Install" to add the extension to VS Code.

### Step 3: Create and Run an ASP.NET Core Project
1. Open Terminal in VS Code by selecting `Terminal` > `New Terminal` from the menu.  
2. Create a new directory for your project: `mkdir MyAspNetApp && cd MyAspNetApp`.  
3. Initialize a new ASP.NET Core web application project: `dotnet new webapp`.  
4. Run the application: `dotnet run`.  
5. Open your browser and navigate to `http://localhost:5000`.

## Optional: Set Up C# Scripting Tools
For quick prototyping or testing ideas without creating a full project, you can use C# scripting tools like `dotnet-script` and `CS-Script`. To set them up, install `dotnet-script` using `dotnet tool install --global dotnet-script` and verify with `dotnet script --version`. Then, install CS-Script tools with `dotnet tool install --global cs-script.cli` and `dotnet tool install --global cs-syntaxer`, and verify using `css --version`. To test, create a script file (e.g., `example.csx`) with content like `Console.WriteLine("Hello, C# Scripting!");` and run it using `dotnet script example.csx` or `css example.csx`. For better integration, install the "CS-Script" extension in VS Code, open the Command Palette (`Ctrl+Shift+P`), and run `"CS-Script: Detect and integrate CS-Script"`.

## Additional Resources
- [Official .NET Documentation](https://learn.microsoft.com/en-us/dotnet/)  
- [Visual Studio Code Documentation](https://code.visualstudio.com/docs)

By following these steps, you should have a fully functional development environment set up for C# and ASP.NET Core on Kali Linux, Windows, or macOS.
