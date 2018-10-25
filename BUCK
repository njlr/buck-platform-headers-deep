genrule(
  name = 'always-fails', 
  out = 'nope.hpp', 
  cmd = 'exit 1', 
)

# cxx_library( # cxx_library seems to be fine
prebuilt_cxx_library(
  name = 'hello', 
  header_namespace = '', 
  header_only = True, 
  exported_headers = [
    'hello.hpp', 
  ], 
  exported_platform_headers = [
    ('nosuchplatform', { 'nope.hpp': ':always-fails' }), 
  ], 
  # srcs = [
  #   'hello.cpp', 
  # ], 
)
