# ARCA_BOX copy on Puhti

There is an installed copy of ARCA_box on CSC Puhti server. If you have access to the project_2004647 you can use this copy.  **Note** the source code of this copy has been modified and there is no warranty for the correctness of the output.

Useful links: 
- [ARCA_BOX Introduction](https://www.helsinki.fi/en/researchgroups/multi-scale-modelling/arca)
- [ARCA_BOX documentation](https://wiki.helsinki.fi/xwiki/bin/view/arca/ARCA%20online%20manual/)
- [ARCA_BOX source code](https://version.helsinki.fi/amg/arca-box)

## Command line interface
### 1. Connect to csc
Refer to [CSC documentation](https://docs.csc.fi/computing/connecting/) on ssh connection
```
# Replace <username> with the name of your CSC user account and
# <host> with "puhti" or "mahti"

ssh <username>@<host>.csc.fi
```

### 2. Change directory
```
cd /projappl/project_2004647/arca-box_shared/
```

### 3. Load necessary modules
```
module load python-data netcdf-c netcdf-fortran
source venv_arcabox/bin/activate
```

### 4. run ARCA from command line
```
./arcabox.exe
```

## Graphic interface
To use GUI, X11 server, for example XQuartz on macOS, should be used to connect Puhti from your laptop.
Then the 1st step:
```
ssh -X <username>@<host>.csc.fi
```
Previous step 2 and 3 are optional because they are included in the script at next step:
```
sh run_arca.sh
```
