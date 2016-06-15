This is a minimum amount of code to reproduce a problem reported on the #lttng channel.

```bash
$ git clone https://github.com/sebhtml/lttng-ust-tracepoint_dlopen_ptr.git
$ mkdir lttng-ust-tracepoint_dlopen_ptr.build
$ cd lttng-ust-tracepoint_dlopen_ptr.build
$ cmake ../lttng-ust-tracepoint_dlopen_ptr
$ make
[ 40%] Built target aligner-lib
[ 60%] Built target aligner
[ 80%] Built target tester-lib
Linking CXX executable tester
libtester-lib.so: undefined reference to `tracepoint_dlopen_ptr'
collect2: error: ld returned 1 exit status
make[2]: *** [tester] Error 1
make[1]: *** [CMakeFiles/tester.dir/all] Error 2
make: *** [all] Error 2
```
