project(
  'lightweight-offscreen',
  'c',
  version : '0.0.1',
  license : 'CC0-1.0',
  meson_version : '>= 1.1',
  default_options : ['c_std=gnu99', 'warning_level=2'],
)

cc = meson.get_compiler('c')

dep_gbm = dependency('gbm')
dep_egl = dependency('egl')
dep_gles2 = dependency('glesv2')

test_list = get_option('test')

test_sources = {
  'lightweight-offscreen' : 'lightweight-offscreen.c',
}

foreach test : test_list
  executable(test,
    join_paths('src', test_sources[test]),
    install : true,
  )
endforeach
