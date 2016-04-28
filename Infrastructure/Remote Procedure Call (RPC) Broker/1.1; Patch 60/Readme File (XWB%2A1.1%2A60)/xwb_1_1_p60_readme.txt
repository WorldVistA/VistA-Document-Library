Readme File
Last Updated: 04/07/2015

============================================================================
Project: VistA Infrastructure (VI) Maintenance FY15 
Software: RPC Broker
Current Version: 1.1
Original Software Release Date: October 1997
Department of Veterans Affairs (VA)
Office of Information and Technology (OI&T)
============================================================================

This file contains any last minute changes, new instructions (not found in
the documentation), and additional information to supplement the manuals.


Read Me for RPC Broker Patch XWB*1.1*60 installation.

NOTE: Current versions of Delphi that are supported by this patch: XE7, 
XE6, XE5, and XE4. These components are only intended for use with the
Delphi for Microsoft Win32 version, and not Win64 or .NET.

This patch is provided as a zip file. To install it in the normal location,
move to the C:\Program Files (x86)\Vista directory. If you are a developer,
you can unzip the file in one location as a saved baseline, and
make a copy in the directory where you are doing your development. Any
updates or changes you make as part of your development should be passed
to the VistA Infrastructure (VI) team for review as a possible change
to future released versions of the BDK.

  1. Rename the existing BDK32 directory to something like BDK32_P50 or
     BDK32_P47 to maintain the existing files.
  2. Unzip the provided zip file, making sure the "use folders" box is
     checked, INTO the Vista directory - this will create the BDK32
     directory and subdirectories under the Vista directory. These files
     and subdirectories can be copied into a BDK32_P60 directory to
     maintain the unmodified files for reference.
  3. After installing the zip file, there should be a BDK32 directory with
     the following subdirectories:
 
       Help - contains help files for developers, updated for this patch.
       Samples - contains sample programs compiled with Delphi XE7
         BrokerEx - contains BrokerExample.exe (includes CCOW and SSH code).
         BSE - contains BseSample1.exe for Broker Security Enhancement.
       Source - contains source code and forms for the components. 
         
  4. After installing the zip file, the BDK32 directory will also contain
     the following executables:

       ServerList.exe - Sample application to edit registry entries for
         VistA servers.
       Clagent.exe - Beta IPv4/IPv6 broker client agent.

  5. Open Delphi.
  6. Enter the directories making sure that the directories are entered into
     the Library fields.
  7. Open the menu Tools | Environment Options.
  8. Select the Library tab [or open the menu Tools | Options and expand the
     Environment Options and then the Delphi Options.
  9. Select Library-Win32].
 10. Press the ellipsis (...) at the right of the combo box for Library Path.
 11. Either enter the directories in the edit box under the list box or press
     the ellipsis at the right of the edit box and migrate to the
     directories. For the default location, these are:
     
       C:\Program Files (x86)\Vista\BDK32
         and
       C:\Program Files (x86)\Vista\BDK32\Source
    
     The BDK32 directory should come before Source in the list.
 12. Press Add.
 13. After entering both directories, press OK to close the dialogue.


If RPCBroker components already exist in the Delphi version:
  1. Select the menu Component | Install Packages.
  2. Select the RPCBroker components (one at time).
  3. Press Remove to remove them.
  4. When finished, press the OK button.


To install the components into Delphi, it is best to compile and build them
in your version of the Delphi IDE so that all of the necessary files are
placed in the proper default directories during installation.  The location
of these default directories may vary depending on the operating system you
are using. In the instructions below, "#" should be replaced with your
version of Delphi (e.g., "#" should be replaced with "7" for Delphi XE7).
To install:
  1. Open Delphi and select the menu File | Close All files, then select
     File | Open, and select the XWB_RX#.dpk file from the BDK32\Source
     directory.  
  2. For the R or run-time files, right-click on the XWB_RX#.bpl file in
     the Project Manager window, then click Compile. Select the menu
     File | Close All (and respond yes if it asks to save changes). [The
     Run-time files should always be compiled first, since the Design-time
     files are dependent upon them].
  3. Select File | Open again to select the Design-time XWB_DX#.dpk file.
     Right-click on the XWB_DX#.bpl file in the Project Manager window,
     then click Build.
  4. Right-click on the XWB_DX#.bpl file in the Project Manager window,
     then click Install to install or update the version of the component.
     Then Close All files (and respond yes if it asks to save changes).
  5. The components are now installed.

