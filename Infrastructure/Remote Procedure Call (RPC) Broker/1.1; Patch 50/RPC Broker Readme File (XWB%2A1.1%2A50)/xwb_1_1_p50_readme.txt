Readme File
Last Updated: 12/02/2013

======================================================
Project: Enhanced VistA Legacy Infrastructure (EVLI)
Maintenance 
Software: RPC Broker
Current Version: 1.1
Original Software Release Date: October 1997
Department of Veterans Affairs (VA)
Office of Information amd Technology (OIT)
Product Development (PD)
======================================================

This file contains any last minute changes, new instructions 
(not found in the documentation), and additional information to
supplement the manuals.


UPDATES
=======

Read Me for RPC Broker Patch XWB*1.1*50 installation.

Note: These components are only intended for use with the Delphi for Microsoft Win32
      version, and not .NET.

This patch is provided as a zip file. To install it in the normal location, move to the
C:\Program Files (x86)\Vista directory.

  1. Rename the existing BDK32 directory to something like BDK32_P50 to maintain the
     existing files.

  2. Unzip the provided zip file, making sure the "use folders" box is checked, INTO
     the Vista directory - this will create the BDK32 directory and subdirectories
     under the Vista directory.

  3. After installing the zip file, there should be a BDK32 directory with the following
     subdirectories: 

       Source  - contains the source code and related files for the components. 
   
       Samples - contains sample programs compiled with Delphi XE5

          BrokerEx     - BrokerExample

          BrokerExCCOW - BrokerExampleCCOW.exe (compiled with the CCOWRPCBroker)
 
          SilentSignOn - contains four programs related to silent or quiet sign-ons.
   
       Help    - contains Broker help files. See the RPC Broker Installation Guide
                 (XWB1_1_IG.pdf) for instructions on how to install the help files.
   
  4. Open Delphi.

  5. Enter the directories making sure that the directories are entered into the Library
     fields.

  6. Open the menu Tools | Options.

  7. Expand the Environment Options and then the Delphi Options.

  8. Select Library.

  9. Press the ellipsis (...) at the right of the combo box for Library Path.

 10. Either enter the directories in the edit box under the list box or press the ellipsis
     at the right of the edit box and migrate to the directories. For the default location,
     these are:
     
       C:\Program Files (x86)\Vista\BDK32 (should be first in the list)
         and
       C:\Program Files (x86)\Vista\BDK32\Source
    
 11. Press Add.

 12. After entering both directories, press OK to close the dialogue.


If RPCBroker components already exist in the Delphi version:

  1. Select the menu Component | Install Packages.

  2. Select the RPCBroker components (one at time).

  3. Press Remove to remove them.

  4. When finished, press the OK button.


To install the components into Delphi, it is best to compile and build them in your
version of the Delphi IDE so that all of the necessary files are placed in the proper
default directories during installation. In the instructions below, "#" should be
replaced with your version of Delphi (e.g., "#" should be replaced with "5" for Delphi
XE5). To install:

  1. Open Delphi and select the menu File | Close All files, then select File | Open, and
     select the XWB_RXE#.dpk file from the BDK32\Source directory.
  
  2. For the R or run-time files, right-click on the XWB_RXE#.bpl file in the Project
     Manager window, then click Compile. Select the menu File | Close All (and respond
     yes if it asks to save changes). [The Run-time files should always be compiled first,
     since the Design-time files are dependent upon them].

  3. Select File | Open again to select the Design-time XWB_DXE#.dpk file.  Right-click on
     the XWB_DXE#.bpl file in the Project Manager window, then click Build.

  4. Right-click on the XWB_DXE#.bpl file in the Project Manager window, then click Install
     to install or update the version of the component.  Then Close All files (and respond
     yes if it asks to save changes).

       - You will now have the following components registered: 

           TCCOWRPCBroker
           TContextorControl
           TRPCBroker
           TXWBRichEdit

  5. If you will be working with the SharedRPCBroker components, select File | Open again
     and select the SharedRPCBroker_RXE#.dpk from the BDK32\Source directory.

  6. Right-click on the SharedRPCBroker_RXE#.bpl file in the Project Manager window, then
     click Compile. Select the menu File | Close All (and respond yes if it asks to save
     changes).

  7. Select File | Open again to select the Design-time SharedRPCBroker_DXE#.dpk file.
     Right-click on the SharedRPCBroker_DXE#.bpl file in the Project Manager window, then
     click Build.

  8. Right-click on the SharedRPCBroker_DXE#.bpl file in the Project Manager window, then
     click Install to install or update the version of the component.  Then Close All
     files (and respond yes if it asks to save changes).

      - You will now have the following components registered:

          TSharedBroker
          TSharedRPCBroker

  9. All RPC Broker components are now installed.