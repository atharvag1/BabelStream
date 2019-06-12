Thread 1 "metababel" received signal SIGSEGV, Segmentation fault.
0x00007ffff77c1679 in clReleaseDevice () from /usr/lib/x86_64-linux-gnu/libOpenCL.so.1
(gdb) backtrace
#0  0x00007ffff77c1679 in clReleaseDevice () from /usr/lib/x86_64-linux-gnu/libOpenCL.so.1
#1  0x00000000004053a8 in cl::detail::ReferenceHandler<_cl_device_id*>::release (device=<optimized out>) at CL/cl2.hpp:1490
#2  cl::detail::Wrapper<_cl_device_id*>::release (this=<optimized out>) at CL/cl2.hpp:1855
#3  cl::detail::Wrapper<_cl_device_id*>::~Wrapper (this=<optimized out>, __in_chrg=<optimized out>) at CL/cl2.hpp:1778
#4  cl::Device::~Device (this=<optimized out>, __in_chrg=<optimized out>) at CL/cl2.hpp:1961
#5  std::_Destroy<cl::Device> (__pointer=<optimized out>) at /usr/include/c++/5/bits/stl_construct.h:93
#6  std::_Destroy_aux<false>::__destroy<cl::Device*> (__last=0x0, __first=0xdb94a0) at /usr/include/c++/5/bits/stl_construct.h:103
#7  std::_Destroy<cl::Device*> (__last=0x0, __first=<optimized out>) at /usr/include/c++/5/bits/stl_construct.h:126
#8  std::_Destroy<cl::Device*, cl::Device> (__last=0x0, __first=<optimized out>) at /usr/include/c++/5/bits/stl_construct.h:151
#9  std::vector<cl::Device, std::allocator<cl::Device> >::~vector (this=0x6158f0 <devices>, __in_chrg=<optimized out>) at /usr/include/c++/5/bits/stl_vector.h:424
#10 0x00007ffff6e89ff8 in __run_exit_handlers (status=0, listp=0x7ffff72145f8 <__exit_funcs>, run_list_atexit=run_list_atexit@entry=true) at exit.c:82
#11 0x00007ffff6e8a045 in __GI_exit (status=<optimized out>) at exit.c:104
#12 0x00007ffff6e70837 in __libc_start_main (main=0x402e40 <main>, argc=1, argv=0x7fffffffde48, init=<optimized out>, fini=<optimized out>, rtld_fini=<optimized out>, stack_end=0x7fffffffde38) at ../csu/libc-start.c:325
#13 0x0000000000403069 in _start ()

