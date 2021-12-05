# I'm trying to port Ubuntu Touch for Xiaomi Redmi 5 (Rosy) using Halium-9.0 - Standalone kernel method

Kernel source: https://github.com/Subash-Baskaran/android_kernel_xiaomi_rosy.git Branch: lineage-17.1

Compilation Scrpit: (This Script) https://github.com/Subash-Baskaran/kernel_compilation_script_rosy

1. I'm following the documentation https://docs.ubports.com/en/latest/porting/introduction/index.html
2. Initializing the build process 
   ./build.sh -b workdir
4. Greeted with below error:
     https://github.com/Subash-Baskaran/kernel_compilation_script_rosy/blob/master/error1
     This was sorted out by adding -no-integrated-as to the make command in ./build/build-kernel.sh
3. Running the script again ./build.sh -b workdir throws new set of errors as below
4.	https://github.com/Subash-Baskaran/kernel_compilation_script_rosy/blob/master/error2
5.	This was sorted out by adding +$(objtree)/scripts/asn1_compiler: $(objtree)/scripts/asn1_compiler.c as specified in here https://patchwork.kernel.org/project/linux-kbuild/patch/1440666497-1420-1-git-send-email-p.fedin@samsung.com/
6. Running the script again ./build.sh -b workdir surprises with below error.
7.	https://github.com/Subash-Baskaran/kernel_compilation_script_rosy/blob/master/error3
8.	For this error google decided not to help me out

can anyone point me in right direction? that would great to me. Thank in advance!

Complete build log can be found here https://github.com/Subash-Baskaran/kernel_compilation_script_rosy/blob/master/complete_log.txt?raw=true
