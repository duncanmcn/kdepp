project('kdepp', 'cpp',
        version : '0.1',
        default_options : ['cpp_std=c++17'])

kdepp_inc = include_directories('include')
kdepp_dep = declare_dependency(include_directories : kdepp_inc)

install_subdir('include/kdepp', install_dir : 'include')

if not meson.is_subproject()
  pkg = import('pkgconfig')
  pkg.generate(name : 'kdepp',
               version : meson.project_version(),
               description : 'Multivariate kernel density estimation for C++')
endif
