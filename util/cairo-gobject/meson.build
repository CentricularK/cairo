cairo_gobject_sources = [
  'cairo-gobject-enums.c',
  'cairo-gobject-structs.c',
]

cairo_gobject_headers = [
  'cairo-gobject.h',
]

libcairogobject = library('cairo-gobject', cairo_gobject_sources,
  c_args: ['-DHAVE_CONFIG_H'],
  include_directories: [incbase, incsrc],
  dependencies: [glib_dep, gobject_dep],
  link_with: [libcairo],
  soversion: '2',
  version: '2.' + ''.join(meson.project_version().split('.')) + '.0',
  install: true,
)

install_headers(cairo_gobject_headers, subdir: 'cairo')
