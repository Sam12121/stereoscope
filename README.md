# Stereoscope

**This is a Prototype! Using this in production will end in tragedy**

A library for working with container image contents, layer file trees, and squashed file trees.

## Getting Started

See `examples/basic.go`

```bash
docker image save centos:8 -o centos.tar
go run examples/basic.go tarball://centos.tar
```

## Why the name?

A stereoscope is a device that takes multiple flat, two-dimensional images to create an impression of a single three-dimensional image. This library takes a container image and gives it depth and detail.

## TODO:

- Add more to the examples dir for lib example usage
- add more to the readme for usage
- use googlecontainer name/tag/repo in parsing and passing of image references to the provider
- update provider to pull() and hasImage() (or introduce something that does this)