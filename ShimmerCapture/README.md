# Shimmer-C-API

# REV0_6
- fix to calibrated time stamp when using 3 byte raw time stamp (e.g. LogAndStream 0.6)

# REV0_5
- major updates to allow API to work with LogAndStream 0.6 and BtStream 0.8, 3 byte raw timestamp

# REV0_4
- minor update to packet loss detection, increasing the limit to 10%
- update to writesamplingrate makes sure internal sensor rates are approximately close/higher than shimmer sampling rate

# REV0_3_2
- Fix to filter, fix to to exg, gui failing when custom gain is used 
- Currently uses ShimmerClosedLibraryRev0_4

# REV0_3_1
- Minor fix to ppgtohr reset
- Currently uses ShimmerClosedLibraryRev0_4

# REV0_3
- Major update to ecgtohr algorithm and filtering algorithm, minor update to ppgtohr algorithm, user should see major improvements in both ecgtohr and ppgtohr algorithms.
- Currently uses ShimmerClosedLibraryRev0_3

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Remove below from official release

BUILDING NOTES
- If new release create a branch with the release number
- Switch output type to Windows Application
- Change Assembly name accordingly ShimmerCapture v0.X
- Update rev in assemblyinfo.cs (follow rev above)
- Update ShimmerClosedLibrary, remove old dll from libs folder and replace with new, update the reference

When releasing a new version the linux - executable has to be compiled in on Shimmer Live machine. To do this.

1) install vmware player

2) download the latest version of the vmware machine 

S:\archive\Shimmer User Resources\Shimmer2r\SUR Content\Firmware Development\VMWare

3) copy the folder to your linux machine, build the project first in windows

4) in the linux machine open a terminal and go to the folder which has the solution file *.sln

5) enter xbuild

6) the executable should now be in the release folder

7) Note, double check your GUI elements, as the mono compiler seems to use different dimensions for panels 

8) To run the application, navigate to the executable file location and type 'mono ShimmerConnect_V0.13.exe' 


For windows

1) Download project from git
2) Build solution and take executable and dlls from Release folder


When releasing
1) zip folder and put in the SUR folder