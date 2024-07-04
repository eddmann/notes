IMAGE = ghcr.io/getzola/zola:v0.17.1
DOCKER = docker run --rm \
	-v $(PWD):/app \
	-v $(PWD)/../books:/app/content/books \
	-v $(PWD)/_index.md:/app/content/books/_index.md \
	-v $(PWD)/../assets:/app/static/assets \
	-w /app

.PHONY: *

serve:
	$(DOCKER) -p 8080:8080 $(IMAGE) serve --interface 0.0.0.0 --port 8080 --base-url 0.0.0.0

build:
	$(DOCKER) $(IMAGE) build
