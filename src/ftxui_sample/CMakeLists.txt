add_executable(intro main.cpp)

target_link_libraries(
  intro
  PRIVATE cpp_project::cpp_project_options
          cpp_project::cpp_project_warnings)

target_link_system_libraries(
  intro
  PRIVATE
          CLI11::CLI11
          fmt::fmt
          spdlog::spdlog
          ftxui::screen
          ftxui::dom
          ftxui::component)

target_include_directories(intro PRIVATE "${CMAKE_BINARY_DIR}/configured_files/include")
