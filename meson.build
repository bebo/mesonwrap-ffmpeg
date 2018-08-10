project('FFmpeg', 'c')

install_data(['bin/avcodec-58.dll',
              'bin/avdevice-58.dll',
              'bin/avfilter-7.dll',
              'bin/avformat-58.dll',
              'bin/avutil-56.dll',
              'bin/ffmpeg.exe',
              'bin/ffplay.exe',
              'bin/ffprobe.exe',
              'bin/postproc-55.dll',
              'bin/swresample-3.dll',
              'bin/swscale-5.dll'], install_dir: '/bin')

cc = meson.get_compiler('c')
# install_data(['bin/jpeg62.dll', 'bin/turbojpeg.dll'], install_dir: '/bin')
libavfilter_dep = declare_dependency(
  version : '7.16.100',
  dependencies : [cc.find_library('avfilter', dirs : meson.current_source_dir() + '/lib')],
  include_directories : include_directories('include'))

libavformat_dep = declare_dependency(
  version: '58.12.100',
  dependencies : [cc.find_library('avformat', dirs : meson.current_source_dir() + '/lib')],
  include_directories : include_directories('include'))

libavutil_dep = declare_dependency(
  version: '56.14.100',
  dependencies : [cc.find_library('avutil', dirs : meson.current_source_dir() + '/lib')],
  include_directories : include_directories('include'))

libavcodec_dep = declare_dependency(
  version: '58.18.100',
  dependencies : [cc.find_library('avcodec', dirs : meson.current_source_dir() + '/lib')],
  include_directories : include_directories('include'))
