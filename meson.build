project('libstdcxx', ['c', 'cpp'])

include_dirs = [
    include_directories('include')
]

arch = get_option('arch')

if arch == 'x86_64'
    include_dirs += [include_directories('include/x86_64-elf')]
endif

libstdxx_dep = declare_dependency(include_directories: include_dirs)

if meson.version().version_compare('>=0.54.0')
    meson.override_dependency('libstdcxx', libstdxx_dep)
endif