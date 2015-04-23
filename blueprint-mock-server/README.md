# Blueprint Mock Server

The blueprint mock server enables easy and automatic mocking of an Markdown API Blueprint specification.

## Usage
By default the image will look for a file called apiary.md located in /usr/src/api-mock and will spin up the server on port 3000. These values are overridable by setting the `PORT` and `MD_PATH` environment variables at runtime.

### Examples
`docker run -p 3000:3000 -e "MD_PATH=./my-api-bp.md" -v $PWD:/usr/src/api-mock -d base2s/blueprint-mock-server:latest`
Port 3000 will be exposed to the host and the server will use my-api-bp.md as its source file located in the current directory.

#### Advanced Functions
- By default the mock server will use the topmost response for a given endpoint. To explicitly test a specific response code in the blueprint set the `prefer=<status code>` header as part of the request.
