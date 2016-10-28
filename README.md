MT6582 Kernel-3.4.67 Source for Gionee M3

    sudo apt-get install ccache
    sudo gedit ~/.bashrc

Add:

    export USE_CCACHE=1
    export CCACHE_DIR=~/android/.ccache

Build:

    sudo chmod -R 777 * ~/android_kernel_gionee_m3-mt6582/arm-eabi-4.8
    cd ~/android_kernel_gionee_m3-mt6582
    export ARCH=arm && export ARCH_MTK_PLATFORM=mt6582 && export CROSS_COMPILE=~/android_kernel_gionee_m3-mt6582/arm-eabi-4.8/bin/arm-eabi- 
    ./mk gionee82_cwet_kk bm_new k


Issue: 

zimage is build sucessfully and when flashed to device then bootlogo loop occurs.
i think zimage is not working due to incomplete files in /kernel-3.4/mediatek/config/gionee82_cwet_kk folder .
