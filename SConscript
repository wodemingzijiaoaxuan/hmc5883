# RT-Thread building script for bridge

from building import *
Import('rtconfig')

src   = []
cwd   = GetCurrentDir()

if GetDepend('PKG_INTF_HMC5883_USING_SENSOR_V1'):
    src += Glob('src/sensor_intf_hmc5883.c')
# add hmc5883 src files.

src += Glob('src/hmc5883.c')

# add hmc5883 include path.
path  = [cwd, cwd + '/inc']

# add src and include to group.
group = DefineGroup('hmc5883', src, depend = ['PKG_USING_HMC5883'], CPPPATH = path)

Return('group')
