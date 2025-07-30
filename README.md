# About This Repository
This repository contains:
* template .gitignore file for usage with TwinCAT 
* best practices XAE environment setup for git integration 
  * [TwinCAT 4024 instructions](source/README_4024.md)
  * [TwinCAT 4026 instructions](source/README_4026.md)

# Template .gitIgnore file
* a base .gitIgnore file was used
  * Created by https://www.toptal.com/developers/gitignore/api/twincat3,visualstudio
* no compiled libraries are included in the git repository except the ones in folder "Compiled Library"
* no tmc files are included in the git repository except the ones in folder "TMC"

## Remark on tmc file(s) inclusion
The .gitIgnore file includes the following tmc rules

    *.tmc
    *.tmcRefac
    #But not these files in any TMC subfolder...
    !**/TMC/*

Per default all *.tmc files are excluded

Check the tmc-file rule if either of the following is true:
   1. You've got TwinCAT C++ projects, as the information in the TMC-file is created manually for the C++ projects (in that case, only (manually) ignore the tmc-files for the PLC projects)
   2. You've created a standalone PLC-project and added events to it, as these are stored in the TMC-file.
   3. shared tmc files are used to exchange data types that should be persisted in the project

## 🧠 Remark on library file(s) inclusion
The .gitIgnore file includes the following tmc rules

    # Create an exception for libraries that are not included in the standard PLC library repository
    # cannot be installed by a TwinCAT function or cannot be downloaded from the Internet!
    *.compiled-library
    *.library
    !**/Compiled Library/*

Per default all library files are excluded except for the ones in any Compiled Library sub folder

# Best practices XAE environment setup for git integration 
See
  * [TwinCAT 4024 instructions](source/README_4024.md)
  * [TwinCAT 4026 instructions](source/README_4026.md)
