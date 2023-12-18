# Sergeev-8-03-hw.
# hello
 
# 1

# tarted by user Сергеев Александр Андреевич
# Running as SYSTEM
# Building in workspace /var/lib/jenkins/workspace/Freestyle Project
# The recommended git tool is: NONE
# No credentials specified
# > git rev-parse --resolve-git-dir /var/lib/jenkins/workspace/Freestyle Project/.git # timeout=10
# Fetching changes from the remote Git repository
# > git config remote.origin.url https://github.com/sergeev-Aleksandr/hw_rename_me.git # timeout=10
# Fetching upstream changes from https://github.com/sergeev-Aleksandr/hw_rename_me.git
# > git --version # timeout=10
# > git --version # 'git version 2.39.2'
# > git fetch --tags --force --progress -- https://github.com/sergeev-Aleksandr/hw_rename_me.git +refs/heads/*:refs/remotes/origin/* # timeout=10
# > git rev-parse refs/remotes/origin/master^{commit} # timeout=10
# Checking out Revision 223dbc3f489784448004e020f2ef224f17a7b06d (refs/remotes/origin/master)
# > git config core.sparsecheckout # timeout=10
# > git checkout -f 223dbc3f489784448004e020f2ef224f17a7b06d # timeout=10
# Commit message: "Update README.md"
# > git rev-list --no-walk 223dbc3f489784448004e020f2ef224f17a7b06d # timeout=10
# [Freestyle Project] $ /bin/sh -xe /tmp/jenkins17193686484774502987.sh
# + /usr/local/go/bin/go test .
# ok      github.com/netology-code/sdvps-materials        (cached)
# [Freestyle Project] $ /bin/sh -xe /tmp/jenkins439670946207586465.sh
# + docker build . -t ubuntu-bionic:8082/hello-world:v2
# DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
#             Install the buildx component to build images with BuildKit:
#             https://docs.docker.com/go/buildx/

# Sending build context to Docker daemon  252.9kB

# Step 1/8 : FROM golang:1.16 AS builder
# 1.16: Pulling from library/golang
# e4d61adff207: Pulling fs layer
# 04ff1945c672b: Pulling fs layer
# ff5b10aec998: Pulling fs layer
# 12de8c754e45: Pulling fs layer
# 8c86ff77a317: Pulling fs layer
# 0395a1c478ba: Pulling fs layer
# 245345d44ed8: Pulling fs layer
# 12de8c754e45: Waiting
# 8c86ff77a317: Waiting
# 0395a1c478ba: Waiting
# 245345d44ed8: Waiting
# 4ff1945c672b: Verifying Checksum
# 4ff1945c672b: Download complete
# ff5b10aec998: Verifying Checksum
# ff5b10aec998: Download complete
# 12de8c754e45: Verifying Checksum
# 12de8c754e45: Download complete
# 8c86ff77a317: Verifying Checksum
# 8c86ff77a317: Download complete
# 245345d44ed8: Verifying Checksum
# 245345d44ed8: Download complete
# e4d61adff207: Download complete
# e4d61adff207: Pull complete
# 4ff1945c672b: Pull complete
# ff5b10aec998: Pull complete
# 12de8c754e45: Pull complete
# 0395a1c478ba: Verifying Checksum
# 0395a1c478ba: Download complete
# 8c86ff77a317: Pull complete
# 0395a1c478ba: Pull complete
# 245345d44ed8: Pull complete
# Digest: sha256:5f6a4662de3efc6d6bb812d02e9de3d8698eea16b8eb7281f03e6f3e8383018e
# Status: Downloaded newer image for golang:1.16
# ---> 972d8c0bc0fc
# Step 2/8 : WORKDIR $GOPATH/src/github.com/netology-code/sdvps-materials
# ---> Running in 34f8fa0eb496
# Removing intermediate container 34f8fa0eb496
# ---> fb8c92ebb17f
# Step 3/8 : COPY . ./
# ---> fab1d5fffe8a
# Step 4/8 : RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix nocgo -o /app .
# ---> Running in d996e1c9a92e
# Removing intermediate container d996e1c9a92e
# ---> 615d904447a3
# Step 5/8 : FROM alpine:latest
# latest: Pulling from library/alpine
# 661ff4d9561e: Pulling fs layer
# 661ff4d9561e: Verifying Checksum
# 661ff4d9561e: Download complete
# 661ff4d9561e: Pull complete
# Digest: sha256:51b67269f354137895d43f3b3d810bfacd3945438e94dc5ac55fdac340352f48
# Status: Downloaded newer image for alpine:latest
# ---> f8c20f8bbcb6
# Step 6/8 : RUN apk -U add ca-certificates
# ---> Running in 989f9d310462
# fetch https://dl-cdn.alpinelinux.org/alpine/v3.19/main/x86_64/APKINDEX.tar.gz
# fetch https://dl-cdn.alpinelinux.org/alpine/v3.19/community/x86_64/APKINDEX.tar.gz
# (1/1) Installing ca-certificates (20230506-r0)
# Executing busybox-1.36.1-r15.trigger
# Executing ca-certificates-20230506-r0.trigger
# OK: 8 MiB in 16 packages
# Removing intermediate container 989f9d310462
# ---> 7acd6913120d
# Step 7/8 : COPY --from=builder /app /app
# ---> ed64f2055e06
# Step 8/8 : CMD ["/app"]
# ---> Running in d158b6b56c15
# Removing intermediate container d158b6b56c15
# ---> a5f208849711
# Successfully built a5f208849711
# Successfully tagged ubuntu-bionic:8082/hello-world:v2
# Finished: SUCCESS
# 
# 
# 
# 
# 
#     2
#  
# 
# pipeline {
# agent any
# stages {
# stage('Git') {
#   steps {git 'https://github.com/netology-code/sdvps-materials.git'}
#  }
#  stage('Test') {
#   steps {
#    sh 'go test .'
#   }
#  }
#  stage('Build') {
#   steps {
#    sh 'docker build . -t ubuntu-bionic:8082/hello-world:v$BUILD_NUMBER'
#   }
#  }
# }
#
#
#
#
#
# Started by user Сергеев Александр Андреевич
# [Pipeline] Start of Pipeline
# [Pipeline] node
# Running on Jenkins in /var/lib/jenkins/workspace/pip
# [Pipeline] {
# [Pipeline] stage
# [Pipeline] { (Git)
# [Pipeline] git
# The recommended git tool is: NONE
# No credentials specified
#  > git rev-parse --resolve-git-dir /var/lib/jenkins/workspace/pip/.git # timeout=10
# Fetching changes from the remote Git repository
#  > git config remote.origin.url https://github.com/netology-code/sdvps-materials.git # timeout=10
# Fetching upstream changes from https://github.com/netology-code/sdvps-materials.git
#  > git --version # timeout=10
#  > git --version # 'git version 2.39.2'
#  > git fetch --tags --force --progress -- https://github.com/netology-code/sdvps-materials.git +refs/heads/*:refs/remotes/origin/* # timeout=10
#  > git rev-parse refs/remotes/origin/master^{commit} # timeout=10
# Checking out Revision da5acf7bcb7f437637adf06fbd03a24dc2c8f13e (refs/remotes/origin/master)
#  > git config core.sparsecheckout # timeout=10
#  > git checkout -f da5acf7bcb7f437637adf06fbd03a24dc2c8f13e # timeout=10
#  > git branch -a -v --no-abbrev # timeout=10
#  > git branch -D master # timeout=10
#  > git checkout -b master da5acf7bcb7f437637adf06fbd03a24dc2c8f13e # timeout=10
# Commit message: "branch main, add creds for vagrant box"
# First time build. Skipping changelog.
# [Pipeline] }
# [Pipeline] // stage
# [Pipeline] stage
# [Pipeline] { (Test)
# [Pipeline] sh
# + go test .
# ok      github.com/netology-code/sdvps-materials        (cached)
# [Pipeline] }
# [Pipeline] // stage
# [Pipeline] stage
# [Pipeline] { (Build)
# [Pipeline] sh
# + docker build . -t ubuntu-bionic:8082/hello-world:v1
# DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
#             Install the buildx component to build images with BuildKit:
#             https://docs.docker.com/go/buildx/
# 
# Sending build context to Docker daemon  245.2kB
# 
# Step 1/8 : FROM golang:1.16 AS builder
#  ---> 972d8c0bc0fc
# Step 2/8 : WORKDIR $GOPATH/src/github.com/netology-code/sdvps-materials
#  ---> Using cache
#  ---> fb8c92ebb17f
# Step 3/8 : COPY . ./
#  ---> 7c6349a88142
# Step 4/8 : RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix nocgo -o /app .
#  ---> Running in 9232441b304b
# Removing intermediate container 9232441b304b
#  ---> 13e339db513b
# Step 5/8 : FROM alpine:latest
#  ---> f8c20f8bbcb6
# Step 6/8 : RUN apk -U add ca-certificates
#  ---> Using cache
#  ---> 7acd6913120d
# Step 7/8 : COPY --from=builder /app /app
#  ---> Using cache
#  ---> ed64f2055e06
# Step 8/8 : CMD ["/app"]
#  ---> Using cache
#  ---> a5f208849711
# Successfully built a5f208849711
# Successfully tagged ubuntu-bionic:8082/hello-world:v1
# [Pipeline] }
# [Pipeline] // stage
# [Pipeline] }
# [Pipeline] // node
# [Pipeline] End of Pipeline
# Finished: SUCCESS
 

