TRAVIS_REPO_SLUG ?= fernandoe/{{cookiecutter.project_slug}}
TAG ?= local

build:
	docker build -t '${TRAVIS_REPO_SLUG}:${TAG}' .

test:
	cd src; pytest -s

ci.test:
	docker run --rm -it '${TRAVIS_REPO_SLUG}:${TAG}' pytest -s; coveralls
