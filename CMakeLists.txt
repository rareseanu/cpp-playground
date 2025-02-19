# set minimum required cmake version 
cmake_minimum_required(VERSION 3.0)

# 
# Specify some user configurable options
# 
OPTION(BUILD_SAMPLES_1_5 "Build the first set of samples" ON)
OPTION(BUILD_SAMPLES_6_9 "Build the second set of samples" ON)
OPTION(BUILD_SAMPLES_10_14 "Build the third set of samples" ON)
OPTION(BUILD_SAMPLES_15_19 "Build the fourth set of samples" ON)
OPTION(BUILD_SAMPLES_EXTERNAL_DEPS "Build the external lib samples" OFF)
OPTION(BUILD_SAMPLES_21_30 "Build the fifth set of samples" ON)

PROJECT(cpp-playground)

IF (BUILD_SAMPLES_1_5)
    ADD_SUBDIRECTORY(01_hello_world)
    ADD_SUBDIRECTORY(02_odd_even)
    ADD_SUBDIRECTORY(03_armstrong)
    ADD_SUBDIRECTORY(04_display_book)
    ADD_SUBDIRECTORY(05_show_args)
ENDIF ()

IF (BUILD_SAMPLES_6_9)
    ADD_SUBDIRECTORY(06_read_file)
    ADD_SUBDIRECTORY(07_matrix_to_console)
    ADD_SUBDIRECTORY(08_lib_ini_read_book)
ENDIF ()
    
IF (BUILD_SAMPLES_10_14)
    ADD_SUBDIRECTORY(10_oop_func_args_book)
    ADD_SUBDIRECTORY(11_oop_book_auth)
ENDIF ()

IF (BUILD_SAMPLES_15_19)
    ADD_SUBDIRECTORY(15_game_of_life)
ENDIF ()

IF (BUILD_SAMPLES_EXTERNAL_DEPS)
    ADD_SUBDIRECTORY(20_sfml_lib_sample)
ENDIF()

IF (BUILD_SAMPLES_21_30)
	ADD_SUBDIRECTORY(21_sample_feline)
	ADD_SUBDIRECTORY(22_sample_kitty_exe)
	ADD_SUBDIRECTORY(24_shared_feline_lib)
	ADD_SUBDIRECTORY(25_shared_lion_lib)
	ADD_SUBDIRECTORY(26_shared_cats)
	ADD_SUBDIRECTORY(27_plugin_lion)
	ADD_SUBDIRECTORY(28_plugin_lynx)
	ADD_SUBDIRECTORY(29_plugin_based_exe)
ENDIF()
