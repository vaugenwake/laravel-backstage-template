build-fpm:
	DOCKER_BUILDKIT=1 docker build -t ${{ values.name }}-fpm:latest -f ./.docker/php/Dockerfile --target=base .

build-nginx:
	DOCKER_BUILDKIT=1 docker build -t ${{ values.name }}-nginx:latest -f ./.docker/nginx/Dockerfile .

build-consumer:
	DOCKER_BUILDKIT=1 docker build -t ${{ values.name }}-consumer:latest -f ./.docker/php/Dockerfile --target=consumer .

build-kube:
	DOCKER_BUILDKIT=1 docker build -t ${{ values.name }}-php:latest -f ./.docker/php/Dockerfile --target=base .
	DOCKER_BUILDKIT=1 docker build -t ${{ values.name }}-consumer:latest -f ./.docker/php/Dockerfile --target=consumer .
	DOCKER_BUILDKIT=1 docker build -t ${{ values.name }}-nginx:latest -f ./.docker/nginx/Dockerfile .
