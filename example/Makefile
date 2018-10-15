IMAGE_NAME=xgboos-sample-project
VERSION=1.0
CONTAINER_NAME=$(IMAGE_NAME)_$(VERSION)
HOST_VOLUME=`pwd`
CONTAINER_VOLUME=/app


build:
	@echo "-----------------------------------------------"
	@echo "Building: " $(IMAGE_NAME):$(VERSION)
	docker build . -t $(IMAGE_NAME):$(VERSION)
	@echo "-----------------------------------------------"

rmi:
	@echo "-----------------------------------------------"
	@echo "Removing Docker Image: " $(IMAGE_NAME):$(VERSION)
	docker rmi $(IMAGE_NAME):$(VERSION)
	@echo "-----------------------------------------------"

start:
	@echo "-----------------------------------------------"
	@echo "Starting Container: " $(IMAGE_NAME)_$(VERSION)
	docker start $(CONTAINER_NAME)
	@echo "-----------------------------------------------"

stop:
	@echo "-----------------------------------------------"
	@echo "Stoping Container: " $(IMAGE_NAME)_$(VERSION)
	docker stop $(CONTAINER_NAME)
	@echo "-----------------------------------------------"

rm:
	@echo "-----------------------------------------------"
	@echo "Removing Container: " $(IMAGE_NAME)_$(VERSION)
	docker rm -f $(CONTAINER_NAME)
	@echo "-----------------------------------------------"

run:
	@echo "-----------------------------------------------"
	@echo "Building: " $(IMAGE_NAME):$(VERSION)
	docker run --name $(CONTAINER_NAME) -v $(HOST_VOLUME):$(CONTAINER_VOLUME) $(IMAGE_NAME):$(VERSION)
	@echo "-----------------------------------------------"

tail:
	@echo "-----------------------------------------------"
	docker logs -f --tail=100 $(CONTAINER_NAME)
	@echo "-----------------------------------------------"

inspect:
	@echo "-----------------------------------------------"
	docker inspect $(CONTAINER_NAME)
	@echo "-----------------------------------------------"

development:
	@echo "-----------------------------------------------"
	@echo "Entering in Docker Container Development Mode: (Ctrl + D to exit)"
	docker run --name $(CONTAINER_NAME) -v $(HOST_VOLUME):$(CONTAINER_VOLUME) --rm -d $(IMAGE_NAME):$(VERSION) tail -f /dev/null
	docker exec -it $(CONTAINER_NAME) /bin/sh
	@echo "-----------------------------------------------"

shell:
	docker exec -it $(CONTAINER_NAME) /bin/sh
