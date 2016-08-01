cmake_minimum_required(VERSION 2.8)
project(RTSIM)

include(ExternalProject)

ExternalProject_Add (
    METASIM
    PREFIX METASIM
    GIT_REPOSITORY "git://github.com/ReTiS-Lab/METASIM.git"
    INSTALL_COMMAND ""
    GIT_TAG "master"
    UPDATE_COMMAND ""
    PATCH_COMMAND ""
    SOURCE_DIR "${CMAKE_SOURCE_DIR}/METASIM"
    TEST_COMMAND ""
)

ExternalProject_Add (
    RTLIB
    DEPENDS METASIM
    GIT_REPOSITORY "git://github.com/ReTiS-Lab/RTLIB.git"
    INSTALL_COMMAND ""
    GIT_TAG "master"
    UPDATE_COMMAND ""
    PATCH_COMMAND ""
    SOURCE_DIR "${CMAKE_SOURCE_DIR}/RTLIB"
    TEST_COMMAND ""
)
