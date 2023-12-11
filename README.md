<div align="center">
   <h1> MiniAiLive Face Recognition Server SDK </h1>
   <img src=https://www.miniai.live/wp-content/uploads/2023/03/logo_name-1-768x426.png alt="MiniAiLive Logo"
   width="300">
</div>

## Welcome to the [MiniAiLive](https://www.miniai.live/)!
We provide system integrators with fast, flexible and extremely precise facial recognition that can be deployed across a number of scenarios, including security, access control, public safety, fintech, smart retail and home protection.
Feel free to use our MiniAI Face Recognition Server SDK.

> **Note**
>
> SDK is fully on-premise, processing all happens on hosting server and no data leaves server.

## Project Structure
```graphql
./MiniAI-Face-Recognition-ServerSDK
  ├─ bin/linux_x86_64                 - # Core library files
  │  ├─ openvino
  │  ├─ libminiai_rec.so
  │  └─ libimutils.so
  ├─ cpp                              - # C++ example
  │  ├─ CMakeLists.txt                - # CMake file for build example
  │  ├─ miniai_rec.h                - # C++ header file to include library
  │  └─ main.cpp                      - # C++ example code
  ├─ flask                            - # Python flask API serving example
  │  ├─ app.py                        - # Flask example code
  │  └─ requirements.txt              - # Python requirement list
  ├─ model                            - # NN dictionary files for library
  │  ├─ data1.bin
  │  ├─ data2.bin  
  │  └─ data3.bin
  ├─ python                           - # Python example
  │  ├─ miniai_rec.py               - # Python library Import Interface file
  │  ├─ main.py                       - # Python example code
  │  └─ requirements.txt              - # Python requirement list
  ├─ test_image                       - # Test Images
  └─ Dockerfile                       - # Docker script for python flask API serving example
```

## Setup Project
#### - Linux
- Download repo and extract it
```
git clone https://github.com/MiniAiLive/MiniAI-Face-Recognition-ServerSDK.git
```
- Install system dependencies
```
sudo apt-get update -y
sudo apt-get install -y libcurl4-openssl-dev libssl-dev libopencv-dev
```
- Copy libraries into system folder
```
cp -rf ./bin/linux_x86_64/openvino/* /usr/lib
cp ./bin/linux_x86_64/libimutils.so /usr/lib
```
#### - Windows
[Contact US](https://www.miniai.live/contact/) by Email info@miniai.live
 
## C++ Example
- Replace license key in main.cpp
- Build project
```
cd cpp
mkdir build && cd build
cmake ..
make
```
- Run project
```
./example_recognition --image1 ../../test_image/Carlos_Menem_0018.jpg --image2 ../../test_image/Carlos_Menem_0020.jpg --model ../../model
```

## Python Example
- Replace license key in main.py
- Install dependencies
```
cd python
pip install -r requirements.txt
```
- Run project
```
python main.py
```
## Python Flask Example
- Replace license key in app.py
- Install dependencies
```
cd flask
pip install -r requirements.txt
```
- Run project
```
python app.py
```
<p align="center">
  <img width="360" src="https://user-images.githubusercontent.com/122285115/212585049-63740d35-e44b-46d4-b02b-fbe4a50fa0e2.png">&emsp;&emsp;
  <img width="360" src="https://user-images.githubusercontent.com/122285115/212585096-8361b446-a0ee-4726-b2f4-906994c17144.png">
</p>


## Docker Flask Example
- Replace license key in app.py
- Build docker image
```
docker build --pull --rm -f "Dockerfile" -t miniairecognition:latest "."
```
- Run image
```
docker run --network host miniairecognition
```
## Request license
Feel free to [Contact US](https://www.miniai.live/contact/)  to get trial License   
You will get email with trial license key ("XXXXX-XXXXX-XXXXX-XXXXX").

## About MiniAiLive
[MiniAiLive](https://www.miniai.live/) is a leading AI solutions company specializing in computer vision and machine learning technologies. We provide cutting-edge solutions for various industries, leveraging the power of AI to drive innovation and efficiency.

## Contact US
For any inquiries or questions, please [Contact US](https://www.miniai.live/contact/)

<p align="center">
<a target="_blank" href="https://t.me/Contact_MiniAiLive"><img src="https://img.shields.io/badge/telegram-@MiniAiLive-blue.svg?logo=telegram" alt="www.miniai.live"></a>&emsp;
<a target="_blank" href="https://wa.me/+19162702374"><img src="https://img.shields.io/badge/whatsapp-MiniAiLive-blue.svg?logo=whatsapp" alt="www.miniai.live"></a>&emsp;
<a target="_blank" href="https://join.skype.com/invite/ltQEVDmVddTe"><img src="https://img.shields.io/badge/skype-MiniAiLive-blue.svg?logo=skype" alt="www.miniai.live"></a>&emsp;
</p>
