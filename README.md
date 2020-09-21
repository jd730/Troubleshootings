# Troubleshooting


* `ImportError: numpy.core.multiarray failed to import`
> Downgrade numpy version to `1.18.0`

* `OpenBLAS blas_thread_init: pthread_create failed for thread 63 of 64: Resource temporarily unavailable`
> ```
> export OMP_NUM_THREADS=1
> export USE_SIMPLE_THREADED_LEVEL3=1
> ```

https://github.com/xianyi/OpenBLAS/issues/1668#issuecomment-402728065

* `ImportError: libGL.so.1: cannot open shared object file: No such file or directory`
> ```
> sudo apt update
> sudo apt -y install libgl1-mesa-glx
> ```
# Tips

* Kill all processes of which names include some `${proc_name}`
> `ps -ef | grep ${proc_name} | grep -v grep | awk '{print $2}' | xargs -r kill -9`
