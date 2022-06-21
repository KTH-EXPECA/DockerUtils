BUILD_CMD = docker buildx build --push --platform linux/arm64,linux/amd64
REPO = $(DOCKER_USER)/iperf3-alpine
TAG = latest

IMG = $(REPO):$(TAG)

all: iperf3-alpine

.PHONY: iperf3-alpine clean

iperf3-alpine: Dockerfile
	$(BUILD_CMD) -t $(IMG) -f $< .

clean:
	docker image rm $(IMG)