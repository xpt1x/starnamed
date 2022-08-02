DOCKER_TAG_NAME:=starname/local

docker_build:
	DOCKER_BUILDKIT=1 docker build --progress=plain -t ${DOCKER_TAG_NAME}:$${STARNAME_VERSION} \
	--build-arg STARNAME_VERSION=$${STARNAME_VERSION} \
	.

1013:
	env STARNAME_VERSION=v0.10.13 make docker_build

p1013:
	env STARNAME_VERSION=v0.10.13 make print_version

1018:
	env STARNAME_VERSION=v0.10.18 make docker_build

p1018:
	env STARNAME_VERSION=v0.10.18 make print_version

1105:
	env STARNAME_VERSION=v0.11.5 make docker_build

p1105:
	env STARNAME_VERSION=v0.11.5 make print_version

docker_build_all: 1013 1018 1105

print_version:
	docker run starname/local:$${STARNAME_VERSION}