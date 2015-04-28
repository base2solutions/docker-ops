# Dredd Test Runner

The dredd test runner enables easy and automatic happy path testing of an API Blueprint specification against a backend implementation.

## Usage
By default the image will look for a file called apiary.md located in /usr/src/dredd and will run against a bakend implementation at http://localhost:8080. These values are overridable by setting the `API_ENDPOINT` and `MD_PATH` environment variables at runtime.

### Examples
`docker run -e MD_PATH=./test-bp.md -e API_ENDPOINT=http://localhost:8081 -v $PWD:/usr/src/dredd/ base2s/dredd:latest`
Dredd will use the test-bp.md spec and run tests against http://localhost:8081/.

