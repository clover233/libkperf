# iOS kperf

A demo shows how to read Intel or Apple M1 CPU performance counter in macOS/iOS.

## How to use

Open a command line window on Mac:
```shell
iproxy 2222 22
```

Create another command-line window:
```shell
ssh -p 2222 root@127.0.0.1
```

After successful cmake, copy the test_perf_decess binary file to your iPhone:
```shell
scp -P 2222 test_perf_process root@127.0.0.1:~
```

Sign in this file:
```shell
ldid -S test_perf_process
```

Output the CPU Counter of all threads for 60 seconds as' output. log ':
```shell
./test_perf_process > output.log 2>&1
```

The CPU Counter for 60 seconds of output thread1 is output1.log: 
```shell
./perf_process <pid>
```

Such as：
```shell
./test_perf_process 1 > output1.log 2>&1
```

## Reference

<https://gist.github.com/ibireme/173517c208c7dc333ba962c1f0d67d12>
