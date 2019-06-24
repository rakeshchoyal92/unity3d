This repository contains docker files to build unity3d.

## Build Script
` docker image build -t IMAGE_NAME:TAG . `

## Run script
Change -v to point to the directory containing your unity project .

```
docker run -it --rm \
--privileged \
-u root \
-e "TEST_PLATFORM=linux" \
-e "WORKDIR=/root/project" \
-p 8080:5900 \
-v "/Users/rakesh/Desktop/work/planimation_forked:/root/project" \
IMAGE_NAME:TAG \
bash 
```