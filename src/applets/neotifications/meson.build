# Neotifications Applet build

applet_neotifications_dir = applets_dir + '.neotifications'

custom_target('plugin-file-neotifications',
    input : 'NeotificationsApplet.plugin.in',
    output : 'NeotificationsApplet.plugin',
    command : [intltool, '--desktop-style', podir, '@INPUT@', '@OUTPUT@'],
    install : true,
    install_dir : applet_neotifications_dir)

applet_neotifications_sources = [
    'NeotificationsApplet.vala',
]

applet_neotifications_deps = [
    libplugin_vapi,
    dep_gtk3,
    dep_peas,
    link_libplugin,
]

shared_library(
    'neotificationsapplet',
    applet_neotifications_sources,
    dependencies: applet_neotifications_deps,
    vala_args: [
        '--pkg', 'libpeas-1.0',
        '--pkg', 'gtk+-3.0',
    ],
    install: true,
    install_dir: applet_neotifications_dir,
)
