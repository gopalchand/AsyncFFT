# AsyncFFT
Use Intel's MKL to perform 2D FFTs in parallel asynchronously on CPU cores

Download the OneAPI Base Toolkit from Intel e.g. https://www.intel.com/content/www/us/en/developer/tools/oneapi/base-toolkit-download.html?operatingsystem=windows&windows-install-type=online
Integrate with Microsoft Visual Studio 2022 (install Visual Studio 2022 if you haven't already done so)
Assume installation in C:\Program Files (x86)\Intel\OneAPI

Create a New Project:
    Open Visual Studio.
    Go to File > New > Project.
    Select Console App and create a new project.

Configure Project Properties:
    Right-click on the project in the Solution Explorer and select Properties.

Set Include Directories:
    Go to Configuration Properties > C/C++ > General.
    Add C:\Program Files (x86)\Intel\oneAPI\2024.1\lib to Additional Include Directories.

Set Library Directories:
    Go to Configuration Properties > Linker > General.
    Add C:\Program Files (x86)\Intel\oneAPI\2024.1\lib to Additional Library Directories.

Go to Configuration Properties > Linker > Input.
  Add the following to Additional Dependencies:
  mkl_intel_lp64.lib
  mkl_sequential.lib
  mkl_core.lib
  libiomp5md.lib

Enable OpenMP:
    Go to Configuration Properties > C/C++ > Language.
    Set OpenMP Support to Yes.
    
Write and Replace Code:
    Replace the content of your main.cpp with the provided code.

Build and Run:
    Build the solution (Build > Build Solution).
    Run the executable (Debug > Start Without Debugging).
