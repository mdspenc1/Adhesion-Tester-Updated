# Adhesion-Tester-Updated
This repository is an updated copy of slehmann1's Adhesion-Tester repository. Since his code is now almost a decade old, there are issues if you try to install it directly from the original repository, especially on newer versions of Windows. In this repository I have created a new installer from scratch, deleted lines 72-77 from the original runSelection.xaml file, and also have provided additional details for installing this application.

# How to Download
Before downloading this application, you need to have .NET Framework  installed on your computer, and it is extremely important to download version 4.5.2 (runtime). You can find the correct download for this .NET version at this link: 
https://dotnet.microsoft.com/en-us/download/visual-studio-sdks?cid=getdotnetsdk. 
It is also necessary to download NI-DAQmx which can be found at this link: 
https://www.ni.com/en/support/downloads/drivers/download.ni-daq-mx.html?srsltid=AfmBOop6dCruJrv8U0EXv5Te9362aR4J_AMuaRTNyNy3bTFZmxO3s7Jj#559060. 
Once you have those installed you can download the installer AdhesionTestInstaller.msi and run it. This will open the setup wizard and allow you to install the application.

# How to Troubleshoot
It is possible that the application might not start once you try opening it. If this is the case, download Visual Studio 2022 (not Visual Studio Code) and copy this repository into your repo folder and open it up as a project. If you get a popup saying that it is incompatible with VS 2022 then choose the middle option to download .NET v4.5.2 (which means you didn't have it installed). Check the references section under the solution and see if there are any warnings next to NationalInstruments.Common or NationalInstruments.DAQmx. If there are, you need to remove those two National Instruments files from the references in your solution, and add them again from your files. These two .dll files will be located in a folder called "National Instruments" (which will likely be in Program Files x86). The directory for NationalInstruments.Common.dll is: National Instruments\Measurement Studio\DotNET\v4.0\AnyCPU\NationalInstruments.Common 19.1.40 and the directory for NationalInstruments.DAQmx is: National Instruments\MeasurementStudioVS2012\DotNET\Assemblies\24.8.45.49159. It might be necessary to delete the repository installer and create a new one, in addition to a signed certificate after the process of re-adding these assembly references, however there are guides for doing this on the internet.

# How to use
Once you have the software installed, plug in your ESP motor controller and find which COM port it connects to in device manager. The default is COM6 but you can change it using the settings tab of adhesion tester. Otherwise it will cause an error when you try to run a trial, and the program will close.

# Original Creator
The original creator of this repository was github user slehmann1. Please visit the original repository at this link for additional details: 
https://github.com/slehmann1/Adhesion-Tester

# Additional Note
Use this link to get the correct version of windows.winMD, download the one for windows 8.1:
https://developer.microsoft.com/en-us/windows/downloads/sdk-archive/
