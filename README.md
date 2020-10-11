# Troubleshooting


* `ImportError: numpy.core.multiarray failed to import`
> `pip install numpy==1.18.0`

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


https://github.com/conda-forge/pygridgen-feedstock/issues/10#issuecomment-365914605

* wandb Segmentation Fault

> `pip install opencv-python==4.3.0.36`

https://github.com/wandb/client/issues/1210


# Tips

* Kill all processes of which names include some `${proc_name}`
> `ps -ef | grep ${proc_name} | grep -v grep | awk '{print $2}' | xargs -r kill -9`

* JW Player change frame rate

```
var video = document.getElementById('exampleId')
var video_speed = video.getElementsByTagName('video')[0]
alert(video_speed.playbackRate)

video_speed.playbackRate=0.2;
```

https://stackoverflow.com/a/18312602
