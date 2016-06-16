This is a minimum amount of code to reproduce a problem reported on the #lttng channel.

```bash
git clone https://github.com/sebhtml/lttng-ust-tracepoint_dlopen_ptr.git

mkdir lttng-ust-tracepoint_dlopen_ptr.build
cd lttng-ust-tracepoint_dlopen_ptr.build
cmake ../lttng-ust-tracepoint_dlopen_ptr
make

lttng create
lttng enable-event -u 'gydle_om:*'
lttng start
./tester
lttng stop
lttng view > trace.txt
cat trace.txt
```
