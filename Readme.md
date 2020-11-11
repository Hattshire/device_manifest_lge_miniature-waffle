LG Bello II Device Manifest
===========================

This manifest goes in ´$(TOP)/.repo/local_manifests/´

Building TWRP v3.1.1 (twrp-4.4)
-------------

1. Be sure to have the proper build tools for your distro, and $JAVA_HOME is set to the correct JDK install.
2. ´repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-4.4´
3. ´git clone repo init --depth=1 -u git://github.com/hattshire/device_manifest_lge_miniature-waffle.git .repo/local_manifests´
4. ´repo sync´
5. ´python2 -m virtualenv .venv´
6. Move line ´te_assert_t *te_assertions;´ from ´$(TOP)/external/checkpolicy/checkpolicy.h´ to ´$(TOP)/external/checkpolicy/checkpolicy.c´
7. ´source .venv/bin/activate´
8. ´source build/envsetup.sh´
9. ´lunch omni_miniwaffle-eng´
10. mka recoveryimage

That's it for now.
