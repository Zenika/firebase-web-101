.PHONY: all install build serve

pwd = $(shell pwd)

install:
	docker pull bpetetot/claat

build:
	docker container run -it -v $(pwd):/app bpetetot/claat export codelab.md

serve: build
	docker container run -it -p 9090:9090 -v $(pwd):/app bpetetot/claat serve -addr 0.0.0.0:9090 codelab.md