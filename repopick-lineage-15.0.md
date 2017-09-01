## # Importer command
#### # source <(curl -Ls https://github.com/AdrianDC/lineage_development_sony8960_master/raw/local_manifests/repopick-lineage-15.0.md)

## # Gerrit without devices and kernels over lineage-15.0*
#### # https://review.lineageos.org/#/q/status:open+branch:%255Elineage-15.0.*+-project:%255ELineageOS/android_device_.*+-project:%255ELineageOS/android_kernel_.*

## # bionic
repopick 185636 185639 185640;

## # bootable/recovery
cd bootable/recovery/;  
git fetch https://review.lineageos.org/LineageOS/android_bootable_recovery refs/changes/17/187717/4 && git checkout FETCH_HEAD;  
cd ../../;

## # build/make
repopick 186687 187329;  
repopick -t releasetools-scripts;  
repopick 187374;

## # build/soong
repopick 186740;

## # external/mksh
repopick 186303;

## # external/toybox
repopick 186302 187155;

## # frameworks/av
repopick 185929 186712 187558 187559 187560 187561;

## # frameworks/base
repopick 186670 186672 186673;

## # frameworks/native
repopick 185671;

## # hardware/qcom/display
repopick 185797 185798 185799;

## # hardware/qcom/gps
repopick 186455 186900 186901;

## # hardware/qcom/wlan
repopick 186300;

## # hardware/qcom/wlan-caf
repopick 187865;

## # hardware/sony/DASH
repopick 186924 186925 186926;

## # packages/apps/Eleven
cd .repo/manifests/;  
git fetch https://review.lineageos.org/LineageOS/android refs/changes/13/187813/1 && git cherry-pick FETCH_HEAD;  
cd ../../;  
repo sync packages/apps/Eleven;  
repopick 187812;

## # packages/apps/Launcher3
cd packages/apps/Launcher3;  
git fetch https://review.lineageos.org/LineageOS/android_packages_apps_Trebuchet refs/changes/18/186918/1 && git cherry-pick FETCH_HEAD;  
cd ../../../;

## # packages/apps/FMRadio
#### # repopick 186688;

## # packages/inputmethods/LatinIME
repopick 187094;

## # system/core
repopick 185642 185654 185672 185653 185656 185657 185658 185659 185888 186684 186304 187146;

## # system/media
repopick 185783;

## # system/sepolicy
repopick 186243 186244 186245 186246 186244 186245;

## # vendor/lineage
repopick 185852 185869 185870 185491 185521 186505;
