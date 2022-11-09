# General Info
qCS is a tool to analyze and alter component values of superconducting logic cells such as RSFQ and AQFP cells. It also helps generating critical margin/yield-optimized variants of designed cells by utilizing the following built-in capabilities such as critical margin calculation, parametric yield analysis and critical margin range optimization.

- The current application version has been developed and tested on CentOS 7 and Windows 10.

# Requirements:
- Certificates (Linux OS only): If the installer doesn't start and the error is about certificates, use the following command:
  $ sudo ln -s /etc/ssl/certs/ca-bundle.trust.crt /etc/ssl/certs/ca-certificates.crt
  
- JoSIM (Linux OS only): It is user's responsibility to satisfy JoSIM requirements (setting up the environment and installing packages). For details, visit https://joeydelp.github.io/JoSIM/#linux
  
- MATLAB Compiler Runtime (MCR) 9.11: The qCS installer will automatically download MCR from Mathworks website. If it is already installed, the system will detect the installed path (Windows OS only). Minimum 2 GB of disk capacity is required to accommodate MCR installation. Any installation directory is permitted for MCR.

- Create a parent folder for qCS installation directory since qCS deletes its parent folder upon uninstallation.

# Setup:
## Linux Instructions
### Preparation for Installation:
1. Extract tar.gz file
	* R-click
	* Open with Archive Manager
	* Select folder
	* L-click [Extract]
	* Select location
	* L-click [Extract]
2. Open folder (example: "qCS_CentOS_2-0")
	* R-click "qCS_installer.install"
	* Properties
	* Tab: Permissions
	* Check: Allow executing file as program
	* Close

### Installation:
1. Open folder which contains the installer (example: "qCS_CentOS_2-0")
	* R-click
	* Open Terminal and write the following:
		* `sudo ./qCS_installer.install`
	* Installation wizard appears
	* Install to a directory (example: /home/userName/qCS_x-x where "x-x" is the version number)

### Permissions:
1. Read/Write Permissions: (if there is a permission restriction while trying to open or run the tool after the installation)
	* Open Terminal on (the installed path/application)
	* Put the following commands which will allow you to change the permissions of the files
		* `sudo chown userName qCS`
		* `sudo chown userName run_qCS.sh`
		* `sudo chown userName jsim`
		* `sudo chown userName jsim_n`
		* `sudo chown userName josim-cli`
	* Make sure that they have read and write permissions by checking their properties
2. There is an alternative method for setting the permissions altogether.
	* Open Terminal in /userName (Home) directory
	* Run one of the following commands using the installation directory
		* `sudo chmod -R a+r+w+x /home/userName/qCS_x-x/` (note: "x-x" is the version number)
		* `sudo chmod 777 -R /home/userName/qCS_x-x/`
	* If Terminal is open in the folder that contains the tool folder qCS_x-x, run one of the following commands instead
		* `sudo chmod -R a+r+w+x qCS_x-x/`
		* `sudo chmod 777 -R qCS_x-x/`

# Reference:
- There are two papers and a book chapter for qCS. One paper and the book chapter are for its algorithm with performance metrics and the second paper is for the tool itself. The related links for them will be provided here once they are published.

# License:
Copyright (C) 2021 Mustafa Altay Karamuftuoglu, Haolin Cong, and Massoud Pedram

SPORT lab, University of Southern California, Los Angeles, CA 90089. All rights reserved.

Permission is hereby granted, without written agreement and without license or royalty fees, to use, copy, and modify, this software and its documentation for any non-commercial purpose, provided that the above copyright notice and the following paragraphs appear in all copies of this software, whether in binary form or not. Commercial use of this software requires written agreement which must be obtained from Massoud Pedram <pedram@usc.edu>.

All trademarks are the property of their respective owners.
Linux is a registered trademark of Linus Torvalds.
Windows is a registered trademark of Microsoft Corporation.
JSIM ..
JoSIM ..
MATLAB ..

IN NO EVENT SHALL THE AUTHORS OR THE UNIVERSITY OF SOUTHERN CALIFORNIA BE LIABLE TO ANY PARTY FOR DIRECT, INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OF THIS SOFTWARE AND ITS DOCUMENTATION, EVEN IF THEY HAVE BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

THE AUTHORS AND THE UNIVERSITY OF SOUTHERN CALIFORNIA SPECIFICALLY DISCLAIM ANY WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE SOFTWARE PROVIDED HEREUNDER IS ON AN "AS IS" BASIS, AND THE AUTHORS HAVE NO OBLIGATION TO PROVIDE MAINTENANCE, SUPPORT, UPDATES, ENHANCEMENTS, OR MODIFICATIONS.

The development of this tool was supported by the Office of the Director of National Intelligence (ODNI), Intelligence Advanced Research Projects Activity (IARPA) SuperTools program, via the U.S. Army Research Office grant W911NF-17-1-0120.

The views and conclusions contained herein are those of the authors and should not be interpreted as necessarily representing the official policies or endorsements, either expressed or implied, of the ODNI, IARPA, or the U.S. Government. The U.S. Government is authorized to reproduce and distribute copies for Governmental purposes notwithstanding any copyright notation herein.
