Readme File
Last Updated: 02/13/2017

============================================================================
Project: VistA Infrastructure (VI) FY17 
Software: RPC Broker
Current Version: 1.1
Original Software Release Date: October 1997
Department of Veterans Affairs (VA)
Office of Information & Technology (OI&T)
Enterprise Program Management Office (EPMO)
============================================================================

This file contains any last minute changes, new instructions (not found in
the documentation), and additional information to supplement the manuals.

Read Me for patch XWB*1.1*65 installation.

NOTE: Current Delphi versions supported by this patch:  
10 Berlin (10.1), 10 Seattle (10.0), XE8, XE7, XE6, XE5, and XE4. 

These components are only intended for use with the Delphi for Microsoft
Win32 version, and not Win64 or .NET.

NOTE: If using FileMan Delphi Components (FMDC) and Kernel Delphi 
Components (KDC), the Broker Development Kit (BDK) needs to be installed 
first, then VA FileMan, and then Kernel.

IMPORTANT NOTE: Unit "Hash" has been renamed "XWBHash" in this version due
to conflicts with a new System.Hash in the Delphi XE8 run time library.
References ("uses") to the "Hash" unit may need to be renamed "XWBHash" in
Delphi applications previously compiled with older versions of the BDK.

This patch is provided as a zip file. To install it in the normal location,
move to the C:\Program Files\Vista directory. If you are a developer, you
can unzip the file in one location as a saved baseline, and make a
copy in the directory where you are doing your development. Any updates or
changes you make as part of your development should be passed to the VistA
Infrastructure (VI) team for review as a possible change to future
released versions of the BDK.

  1. Back up the existing BDK32 directory by renaming it (e.g., BDK32_P60 or
     BDK32_P50) in order to maintain the existing files.
  
  2. Unzip the provided zip file, making sure the "use folders" box is
     checked, INTO the Vista directory - this will create the BDK32
     directory and subdirectories under the Vista directory. These files
     and subdirectories can be copied into a BDK32_P65 directory to
     maintain the unmodified files for reference.
  
  3. After installing the zip file, there should be a BDK32 directory with
     the following subdirectories:
 
       * BAPI32dll - Contains BAPI32.DLL and sample header files.
        
       * Help - Contains help files for developers, updated for this patch.
       
       * Samples - Contains sample programs compiled with Delphi XE8:
           
           - BrokerEx: Contains BrokerExample.exe (includes CCOW and 
             SSH code) demonstrating Delphi GUI for VistA using 2-factor 
             authentication (2FA).
           
           - BSE: Contains BseSample1.exe for Broker Security 
             Enhancement (BSE).
       
       * Source - contains source code and forms for the components.
         
  4. Open Delphi.
  
  5. Enter the directories making sure that the directories are entered into
     the Library fields.
  
  6. Open the menu Tools | Environment Options.
  
  7. Select the Library tab [or open the menu Tools | Options and expand the
     Environment Options and then the Delphi Options.
  
  8. Select Library-Win32].
  
  9. Press the ellipsis (...) at the right of the combo box for Library Path.
  
 10. Either enter the directories in the edit box under the list box or press
     the ellipsis at the right of the edit box and migrate to the
     directories. For the default location, this is:
     
       C:\Program Files (x86)\Vista\BDK32\Source
    
 11. Press Add.
 
 12. After entering the directory, press OK to close the dialogue.


If RPCBroker components already exist in the Delphi version:
  
  1. Select the menu Component | Install Packages.
  
  2. Select the RPCBroker components (one at time).
  
  3. Press Remove to remove them.
  
  4. When finished, press the OK button.


To install the components into Delphi, it is best to compile and build them
in your version of the Delphi IDE, so that all of the necessary files are
placed in the proper default directories during installation.  The location
of these default directories can vary depending on the operating system you
are using. The DesignTime package bundles the RunTime package into components
that are used when building applications, so the RunTime package must be
compiled before the DesignTime package is compiled and installed.

For your convenience, there are XWB_RXE* (RunTime) and XWB_DXE* (Design Time)
projects set up for specific versions of Delphi, which may help resolve some
access violation errors for run time libraries in some versions. The
XWB_RunTime and XWB_DesignTime projects are for Delphi 10 and 10.1.

To install:
  
  1. Open Delphi and select the menu File | Close All files, then select
     File | Open, and select the XWB_RunTime.dpk file from the BDK32\Source
     directory.
    
  2. For the R or run-time files, right-click on the XWB_RunTime.bpl file
     in the Project Manager window, then click Compile. Select the menu
     File | Close All (and respond yes if it asks to save changes). [The
     Run-time files should always be compiled first, since the Design-time
     files are dependent upon them].
  
  3. Select File | Open again to select the Design-time XWB_DesignTime.dpk
     file. Right-click on the XWB_DesignTime.bpl file in the Project
     Manager window, then click Build.
  
  4. Right-click on the XWB_DesignTime.bpl file in the Project Manager window,
     then click Install to install or update the version of the component.
     Then Close All files (and respond yes if it asks to save changes).
  
  5. The components are now installed.

The file "IAMBase.inc" contains constants (defaults) used for delegated 2-factor
authentication (Identity and Access Management). This file can be edited if
implementation is being tested in a non-production environment with different
values.