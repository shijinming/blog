---
title: tensorflow中测试GPU方法
date: 2018-06-18 00:06:48
categories:
- Python
- 环境配置
tags:
- Python
- Tensorflow
- 环境配置
---
``` python
def is_gpu_available(cuda_only=True):
  from tensorflow.python.client import device_lib as _device_lib

  if cuda_only:
    return any((x.device_type == 'GPU')
               for x in _device_lib.list_local_devices())
  else:
    return any((x.device_type == 'GPU' or x.device_type == 'SYCL')
               for x in _device_lib.list_local_devices())

def get_available_gpus():
    from tensorflow.python.client import device_lib as _device_lib
    local_device_protos = _device_lib.list_local_devices()
    return [x.name for x in local_device_protos if x.device_type == 'GPU']
```