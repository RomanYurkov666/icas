# Welcome to iCAS

Please head over to our [documentation](https://ecg-icas.github.io/icas/doc/prod/).

### Making changes to the API documentation
For changes to the **freeform part** of the documentation (**anything under src/**), `sphinx-build` version 6.1.3 is required. 

Run
```
make install
```
to make sure the necessary html files are generated properly.
 
For changes to the **API reference endpoints**, change the `.yaml` file(s) directly under the `/openapi` folder.
The component schemas are organized in separate folders per logical domain, with the request and responses models decoupled.
**There is no need to run anything** to have the changes properly rendered in this case.

To help you understand the OpenAPI specification, you can [interactively explore it](https://openapi-map.apihandyman.io/?version=3.0).
Version `3.0.0` of the OpenAPI specification is currently used.
The most popular IDEs for development have an OpenAPI plugin, which helps with validation issues and visual inspection of the API.
[Here](https://plugins.jetbrains.com/plugin/14837-openapi-swagger-editor) is one for IntellJ IDEA.
Alternatively, the web [Swagger editor](https://editor.swagger.io/) can help to surface any errors quickly, but is limited to a single file.

Release follows standard procedure: add changes to new branch, create a PR and get required approvals, finally merge to `gh-pages`.

Please **make sure to resolve any linter errors and warnings** before merging changes to the main `gh-pages` branch.

(c) 2015 - The iCAS Team
