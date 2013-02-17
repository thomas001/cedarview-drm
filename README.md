cedarview-drm
=============

Yet another try to run Intel's cdv driver on newer kernels. Instead of patching the driver to work with newer drm modules, we port the drm module from linux 3.2 to newer kernels. This is basically the approach used by the ubuntu packages: http://packages.ubuntu.com/source/precise-updates/cedarview-drm-drivers

I only did basic patching, layout for drm backport is due to the cedarview-drm-drivers package's authors.

Kernel versions
---------------

Currently the following kernel versions are tested:

 * vanilla 3.7.8
 * vanilla 3.4.32 --- *use `linux-3.5` branch*
 * ubuntu's 3.5.0-23-generic --- *use `linux-3.5` branch*

How to use
---------

You can either compile the module directly using a command like 

    make -C /lib/modules/`uname -r`/build M=`pwd` KMYDIR=`pwd`

or you employ dkms:

    cp -r /path/too/cedarview-drm /usr/src/cedarview-drm-1.0.3
    dkms add cedarview-drm/1.0.3

Afterwards you have to build the module and maybe regenerate your initrd. In ubuntu this would be

    sudo dpkg-reconfigure linux-image-`uname -r`


    
