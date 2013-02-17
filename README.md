cedarview-drm
=============

Yet another try to run Intel's cdv driver on newer kernels. Instead of patching the driver to work with newer drm modules, we port the drm module from linux 3.2 to newer kernels. This is basically the approach used by the ubuntu packages: http://packages.ubuntu.com/source/precise-updates/cedarview-drm-drivers

I only did basic patching, layout for drm backport is due to the cedarview-drm-drivers package's authors.
