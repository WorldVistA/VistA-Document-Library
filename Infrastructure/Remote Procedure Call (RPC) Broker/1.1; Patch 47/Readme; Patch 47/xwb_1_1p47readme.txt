Readme File
Last Updated: 07/07/2008

==================================================
Project: ISS Maintenance FY08 (Enhance Infrastructure Legacy VistA) 
Software: RPC Broker
Current Version: 1.1
Original Software Release Date: October 1997
Department of Veterans Affairs
Office of Information & technology (OI&T)
==================================================

This file contains any last minute changes, new instructions 
(not found in the documentation), and additional information to
supplement the manuals.


UPDATES
=======

 * 07/02/08: BDK Supports CCOW Broker (Patches XWB*1.1*35 & 40), Delphi V. 7.0, SSO/UC (replaces ESSO support),
             and non-callback functionalityRead Me for patch XWB*1.1*47 installation.

Note: If you are using Delphi 2005, 2006, or 2007, these components are only intended for use with the Delphi for Microsoft Win32 version, and not .NET.

This patch is provided as a zip file. To install it in the normal location, move to the C:\Program Files\Vista directory.

  1. Rename the existing BDK32 directory to something like BDK32_P40 to maintain the existing files.
  2. Unzip the provided zip file, making sure the "use folders" box is checked, INTO the Vista directory - this will create the BDK32 directory and subdirectories under the Vista directory.

  3. After installing the zip file, there should be a BDK32 directory with the following subdirectories: 

       Source - contains the source code and related files for the components. 
   
       Samples - contains sample programs compiled with Delphi 5
          BrokerEx - contains BrokerExample and BrokerExampleCCOW (compiled with
                     the CCOWRPCBroker) 
          SilentSignOn - contains four programs related to silent or quiet sign-ons.
   
       Samples D2006 - contains the same sample programs compiled with Delphi 2006.

       Bin - contains the bpl and dcp files for the components and D directories for Delphi 5, 6, 7, 2005, 2006, and 2007 contains the compiled units and forms for a specified version of Delphi.
   
  4. Open Delphi.
  5. Enter the directories making sure that the directories are entered into the Library fields.
  6. Open the menu Tools | Environment Options.
  7. Select the Library tab [or open the menu Tools | Options and expand the Environment Options and then the Delphi Options.
  8. Select Library-Win32].
  9. Press the ellipsis (...) at the right of the combo box for Library Path.
 10. Either enter the directories in the edit box under the list box or press the ellipsis at the right of the edit box and migrate to the directories. For the default location, these are:
     
     C:\Program Files\Vista\BDK32\Dnumber  (where number is 5, 6, 7, 2005, 2006, or 2007)
    
     and
    
     C:\Program Files\Vista\BDK32\Source
    
     The Dnumber directory should come first in the list.
 11. Press Add.
 12. After entering both directories, press OK to close the dialogue.


If RPCBroker components already exist in the Delphi version:
  1. Select the menu Component | Install Packages.
  2. Select the RPCBroker components (one at time).
  3. Press Remove to remove them.
  4. When finished, press the OK button.


There are two ways to install the components into a version of Delphi: 

  1. The first method of installing the components
     a. Open Delphi.
     b. Select the menu Component | Install Packages.
     c. Press the Add button.
     d. Migrate to the location of the bpl file for the component (this would be the Design-time file (Dnumber.bpl).  The run-time or Rnumber files are not selected, but are used by the Design-time files. These could be selected from the BDK32\Bin directory, or the files could be copied to the location normally used by Delphi [for Delphi 5, 6, or 7, this location is:
    
   C:\Program Files\Borland\Delphi5\Projects\Bpl (where 5 could be 6 or 7),
   
   For Delphi 2005 to 2007, this location is:

   C:\Documents and Settings\username\My Documents\Borland Studio Projects\Bpl
   
     e. Select the XWB_D50.bpl (or 60, 70, 2005, 2006, or 2007 as appropriate) file.
     f. Press the Open button. This adds it to the list of active components. While most developers would only need that set of components, the SharedRPCBroker_D50.bpl (or other numbers) file can then be selected if the SharedRPCBroker components are desired as well.


  2. The second method of installing the components is the same as would be used to update a component when something that affects it has changed.
     a. Open Delphi.
     b. Select the menu File | Close All files.
     c. Select File | Open.
     d. Select the XWB_Rnumber.dpk file from the BDK32\Source directory (where number is the appropriate number for the version of Delphi). The package dialogue will open, for the R or run-time files.
     e. Press Compile.
     f. Close the dialogue (the Run-time files should always be compiled first, since the Design-time files are dependent upon them).
     g. Select the menu File | Open.
     h. Select the corresponding Design-time or D file. The package dialogue will open.
     e. Press Compile.
     f. Press the Install button to install or update the version of the component.
     g. Select Close. The components are now installed.
