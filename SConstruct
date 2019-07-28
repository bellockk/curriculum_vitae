env = Environment()
common = 'common'
env.PrependENVPath('PATH', common)
env.Append(LATEXFLAGS=['-halt-on-error', '-shell-escape'],
           TEXINPUTS=[common])
Export('env')
doc = SConscript('src/SConscript', variant_dir='build', duplicate=0)
Install('dist', doc)
