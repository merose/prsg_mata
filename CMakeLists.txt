cmake_minimum_required(VERSION 2.8.3)
project(prsg_mata)

find_package(catkin REQUIRED)

if (CATKIN_ENABLE_TESTING)
  catkin_add_nosetests(tests)
endif()

if (CATKIN_ENABLE_TESTING)
  find_package(rostest REQUIRED)
#  add_rostest(tests/your_first_rostest.test)
#  add_rostest(tests/your_second_rostest.test)
endif()

catkin_package()

catkin_install_python(
    PROGRAMS
	nodes/prsg_controller
    DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

catkin_python_setup()
