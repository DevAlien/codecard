# Project name, programming language and version
project (
    'com.github.devalien.codecard',
    'vala', 'c',
    version: '0.0.1'
)

# Translation module
i18n = import ('i18n')

# Project arguments
add_project_arguments (
    '-DGETTEXT_PACKAGE="@0@"'.format (meson.project_name ()),
    language: 'c'
)


gnome = import('gnome')

asresources = gnome.compile_resources(
    'as-resources', 'data/gresource.xml',
    source_dir: 'data',
    c_name: 'as'
)

# Listing dependencies
dependencies = [
    dependency ('glib-2.0'),
    dependency ('gtk+-3.0'),
    dependency ('gee-0.8'),
    dependency ('granite'),
    dependency ('gtksourceview-3.0')
]

subdir ('src')

# Executable
executable (
    meson.project_name (),
    sources,
    asresources,
    dependencies: dependencies,
    install: true
)

subdir ('data')
subdir ('po')

meson.add_install_script ('meson/post_install.py')
