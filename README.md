This repository contains docker files to build unity3d.

## Build Script
` docker image build -t IMAGE_NAME:TAG . `

## Run script
- Change -v to point to the directory containing your unity project

```
export UNITY_IMAGE=rakeshchoyal92/unity3d:latest
docker run -it -v "/home/ubuntu/frontend:/root/project/frontend" unity:0.1 \
'/opt/Unity/Editor/Unity' -quit -batchmode -nographics \
-projectPath /root/project/frontend \
-executeMethod Buildscript.Build -logFile
```