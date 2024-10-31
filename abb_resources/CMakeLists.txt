cmake_minimum_required(VERSION 3.8)
project(abb_resources)

find_package(ament_cmake REQUIRED)

install(
  DIRECTORY urdf
  DESTINATION share/${PROJECT_NAME}
)

ament_export_dependencies(${THIS_PACKAGE_INCLUDE_DEPENDS})

if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  list(APPEND AMENT_LINT_AUTO_EXCLUDE
      ament_cmake_copyright
  )
  ament_lint_auto_find_test_dependencies()
endif()

ament_package()
