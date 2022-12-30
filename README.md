# OTC_ECS_AI-Benchmark
AI Benchmark on one of the flavor's of Open Telekom Cloud's Elastic Cloud Server : https://open-telekom-cloud.com/de/produkte-services/core-services/elastic-cloud-server  
Opensource projects: https://pypi.org/project/ai-benchmark/  
Specs:  
OTC - ECS  
Flavor p2.2xlarge.8  
OS: Standard_Ubuntu_22.04_V100_latest  
CPU/RAM: 8 vCPUs | 64 GiB  


`~# lspci -v | grep -E -i --color 'VGA|3d|2d'
00:02.0 VGA compatible controller: Cirrus Logic GD 5446 (prog-if 00 [VGA controller])
        Prefetchable memory behind bridge: 0000001802c00000-0000001802dfffff [size=2M]
00:0d.0 3D controller: NVIDIA Corporation GV100GL [Tesla V100 PCIe 16GB] (rev a1)`


`$ python3 ai-benchmark.py  

2022-12-27 07:24:12.378411: I tensorflow/core/platform/cpu_feature_guard.cc:193] This TensorFlow binary is optimized with oneAPI Deep Neural Network Library (oneDNN) to use the following CPU instructions in performance-critical operations:  AVX2 FMA
To enable them in other operations, rebuild TensorFlow with the appropriate compiler flags.
2022-12-27 07:24:13.561084: W tensorflow/compiler/xla/stream_executor/platform/default/dso_loader.cc:64] Could not load dynamic library 'libnvinfer.so.7'; dlerror: libnvinfer.so.7: cannot open shared object file: No such file or directory
2022-12-27 07:24:13.561190: W tensorflow/compiler/xla/stream_executor/platform/default/dso_loader.cc:64] Could not load dynamic library 'libnvinfer_plugin.so.7'; dlerror: libnvinfer_plugin.so.7: cannot open shared object file: No such file or directory
2022-12-27 07:24:13.561211: W tensorflow/compiler/tf2tensorrt/utils/py_utils.cc:38] TF-TRT Warning: Cannot dlopen some TensorRT libraries. If you would like to use Nvidia GPU with TensorRT, please make sure the missing libraries mentioned above are installed properly.`

>>   AI-Benchmark-v.0.1.2
>>   Let the AI Games begin..

*  TF Version: 2.11.0
*  Platform: Linux-5.15.0-50-generic-x86_64-with-glibc2.35
*  CPU: N/A
*  CPU RAM: 63 GB

The benchmark is running...
The tests might take up to 20 minutes
Please don't interrupt the script

1/19. MobileNet-V2

1.1 - inference | batch=50, size=224x224: 543 ± 22 ms
1.2 - training  | batch=50, size=224x224: 2658 ± 29 ms

2/19. Inception-V3

2.1 - inference | batch=20, size=346x346: 1425 ± 18 ms
2.2 - training  | batch=20, size=346x346: 6884 ± 40 ms

3/19. Inception-V4

3.1 - inference | batch=10, size=346x346: 1413 ± 11 ms
3.2 - training  | batch=10, size=346x346: 6446 ± 17 ms

4/19. Inception-ResNet-V2

4.1 - inference | batch=10, size=346x346: 1543 ± 8 ms
4.2 - training  | batch=8, size=346x346: 5824 ± 31 ms

5/19. ResNet-V2-50

5.1 - inference | batch=10, size=346x346: 919 ± 6 ms
5.2 - training  | batch=10, size=346x346: 4062 ± 24 ms

6/19. ResNet-V2-152

6.1 - inference | batch=10, size=256x256: 1353 ± 11 ms
6.2 - training  | batch=10, size=256x256: 6642 ± 45 ms

7/19. VGG-16

7.1 - inference | batch=20, size=224x224: 2687 ± 21 ms
7.2 - training  | batch=2, size=224x224: 2210 ± 12 ms

8/19. SRCNN 9-5-5

8.1 - inference | batch=10, size=512x512: 2427 ± 14 ms
8.2 - inference | batch=1, size=1536x1536: 2183 ± 10 ms
8.3 - training  | batch=10, size=512x512: 20440 ± 969 ms

9/19. VGG-19 Super-Res

9.1 - inference | batch=10, size=256x256: 4595 ± 11 ms
9.2 - inference | batch=1, size=1024x1024: 7320 ± 14 ms
9.3 - training  | batch=10, size=224x224: 20997 ± 230 ms

10/19. ResNet-SRGAN

10.1 - inference | batch=10, size=512x512: 3964 ± 10 ms
10.2 - inference | batch=1, size=1536x1536: 3566 ± 12 ms
10.3 - training  | batch=5, size=512x512: 8814 ± 56 ms

11/19. ResNet-DPED

11.1 - inference | batch=10, size=256x256: 4503 ± 15 ms
11.2 - inference | batch=1, size=1024x1024: 7224 ± 14 ms
11.3 - training  | batch=15, size=128x128: 9915 ± 32 ms

12/19. U-Net

12.1 - inference | batch=4, size=512x512: 8818 ± 10 ms
12.2 - inference | batch=1, size=1024x1024: 9259 ± 389 ms
12.3 - training  | batch=4, size=256x256: 8844 ± 130 ms

13/19. Nvidia-SPADE

13.1 - inference | batch=5, size=128x128: 3172 ± 36 ms
13.2 - training  | batch=1, size=128x128: 3053 ± 33 ms

14/19. ICNet

14.1 - inference | batch=5, size=1024x1536: 2558 ± 48 ms
14.2 - training  | batch=10, size=1024x1536: 7068 ± 213 ms

15/19. PSPNet

15.1 - inference | batch=5, size=720x720: 16307 ± 60 ms
15.2 - training  | batch=1, size=512x512: 6316 ± 19 ms

16/19. DeepLab

16.1 - inference | batch=2, size=512x512: 3497 ± 14 ms
16.2 - training  | batch=1, size=384x384: 4666 ± 342 ms

17/19. Pixel-RNN

17.1 - inference | batch=50, size=64x64: 2701 ± 13 ms
17.2 - training  | batch=10, size=64x64: 2315 ± 521 ms

18/19. LSTM-Sentiment

18.1 - inference | batch=100, size=1024x300: 7094 ± 45 ms
18.2 - training  | batch=10, size=1024x300: 14620 ± 1006 ms

19/19. GNMT-Translation

19.1 - inference | batch=1, size=1x20: 3263 ± 23 ms

Device Inference Score: 443
Device Training Score: 467
Device AI Score: 910

For more information and results, please visit http://ai-benchmark.com/alpha
