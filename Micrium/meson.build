project('uCOS-III_POSIX', 'c')

my_inc = include_directories(['Examples/POSIX/GNU/OS3',
       'Software/uC-CPU',
       'Software/uC-CPU/Posix/GNU',
       'Software/uC-LIB',
       'Software/uCOS-III/Source',
       'Software/uCOS-III/Ports/POSIX/GNU'])

my_dep = declare_dependency(include_directories : my_inc)

pthread_dep = dependency('threads')

src = ['Examples/POSIX/GNU/OS3/app.c',
       'Examples/POSIX/GNU/OS3/os_app_hooks.c',

       'Software/uC-CPU/cpu_core.c',
       'Software/uC-CPU/Posix/GNU/cpu_c.c',

       'Software/uC-LIB/lib_ascii.c',
       'Software/uC-LIB/lib_math.c',
       'Software/uC-LIB/lib_mem.c',
       'Software/uC-LIB/lib_str.c',

       'Software/uCOS-III/Source/os_cfg_app.c',
       'Software/uCOS-III/Source/os_core.c',
       'Software/uCOS-III/Source/os_dbg.c',
       'Software/uCOS-III/Source/os_flag.c',
       'Software/uCOS-III/Source/os_int.c',
       'Software/uCOS-III/Source/os_mem.c',
       'Software/uCOS-III/Source/os_mon.c',
       'Software/uCOS-III/Source/os_msg.c',
       'Software/uCOS-III/Source/os_mutex.c',
       'Software/uCOS-III/Source/os_pend_multi.c',
       'Software/uCOS-III/Source/os_prio.c',
       'Software/uCOS-III/Source/os_q.c',
       'Software/uCOS-III/Source/os_sem.c',
       'Software/uCOS-III/Source/os_stat.c',
       'Software/uCOS-III/Source/os_task.c',
       'Software/uCOS-III/Source/os_tick.c',
       'Software/uCOS-III/Source/os_time.c',
       'Software/uCOS-III/Source/os_tmr.c',
       'Software/uCOS-III/Source/os_var.c',

       'Software/uCOS-III/Ports/POSIX/GNU/os_cpu_c.c']


executable('demo', src, link_args : '-lrt', dependencies : [my_dep, pthread_dep])