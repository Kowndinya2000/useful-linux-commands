### Observe GPU Memory Usage on CUDA Device:0 on a loop
````
while true; do   mem=$(nvidia-smi --query-gpu=memory.used --format=csv,noheader,nounits | sed -n '1p');   echo "GPU 0 Memory Used: ${mem} MiB";   sleep 1; done
````
> --query-gpu=memory.used — gets used memory for all GPUs.

> --format=csv,noheader,nounits — removes units and header (just raw numbers).

> sed -n '1p' — prints only the first line, corresponding to GPU 0.

