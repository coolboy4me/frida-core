interfaces_sources = [
  'session.vala',
]

extra_deps = []
if host_os_family != 'windows'
  extra_deps += [gio_unix_dep]
endif

interfaces = static_library('frida-interfaces', interfaces_sources,
  vala_header: 'frida-interfaces.h',
  dependencies: [glib_dep, gobject_dep, gio_dep] + extra_deps,
)

interfaces_dep = declare_dependency(
  include_directories: include_directories('.'),
  link_with: interfaces,
)

interfaces_build_dir = meson.current_build_dir()
