project('libstdc++', 'c', 'c++',)

libstdcxx_incs = [
    include_directories('libstdc++')
]

if get_option('arch') == "amd64"
    libstdcxx_incs += include_directories('libstdc++/x86_64-elf')
endif

libstdcxx_dep = declare_dependency(include_directories: libstdcxx_incs)

if meson.version().version_compare('>=0.54.0')
    meson.override_dependency('libstdcxx_headers', libstdcxx_headers_dep)
endif