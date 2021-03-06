# Metadata API

[![continuous integration status](https://travis-ci.org/alphagov/metadata-api.svg?branch=master)](http://travis-ci.org/alphagov/metadata-api)

A small HTTP application that acts as an easy way to get metadata
about given URLs on [GOV.UK](https://www.gov.uk/).

## Requirements

To run the code you will need to have at least Go 1.2 installed.

## Development

You can run the tests locally by running the following to use
`third_party.go` to fetch the dependencies:

```bash
make
```

Alternatively you can install the dependencies directly to your
`$GOPATH` and run the tests using:

```bash
go get -v ./...
go test -v ./...
```

## Running

You can build a binary using either `make build` or `go build`. You
should then be able to run the binary directly.

### Configuration

Most configuration can be handled using `ENV` variables that get
passed into the process. However the `BEARER_TOKEN` values for both
the Content API and the Need API are provided using a JSON file in the
working directory of the process. See `config.json` for an example of
this file.
