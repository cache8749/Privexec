# privexec

add_executable(
  Privexec WIN32
  alias.cc
  capabilities.cc
  app.cc
  main.cc
  Privexec.manifest
  Privexec.rc)

target_link_libraries(
  Privexec
  Exec
  belashl
  Comctl32
  Shlwapi
  Pathcch
  wtsapi32
  Userenv
  Taskschd
  Kernel32
  Gdi32
  Advapi32)

install(TARGETS Privexec DESTINATION .)
