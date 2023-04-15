cmake_minimum_required(VERSION 3.4.1)
project(VINSMobile)

# done here so it's not necessary for every target_link_library call of opencv
SET(OpenCV_DIR /data/gitRepository/VINS-Mobile-Android/app/libs/VINS-Mobile-master/VINS_ThirdPartyLib/opencv-4.5.0-android-sdk/OpenCV-android-sdk/sdk/native/jni)
find_package(OpenCV REQUIRED)

# this is branching into all the subdirectories and thus connecting them all
add_subdirectory(VINS_ThirdPartyLib)
add_subdirectory(ThirdParty/DBoW)
add_subdirectory(ThirdParty/DUtils)
add_subdirectory(ThirdParty/DVision)
add_subdirectory(VINS_ios)