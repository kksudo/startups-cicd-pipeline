## python/

It's a submodule of the most popular '[Full Stack FastAPI Template](https://github.com/tiangolo/full-stack-fastapi-template/tree/master/backend)' git repository. In this case we focus only on the backend part of the project.
This dir does not include any changes from my side. It's just a copy of the original project. 



### Differences from the original project

In spite of the fact that the project already have automation we will create a new one to make the deployment process easier to use best 
practices.

- **docker/python/Dockerfile**: We will use a production ready slim container with only application(without migrations, tests, etc).
- **docker/python/Dockerfile.full**: We will use a development container with all dependencies like tests, migrations, etc.
- **docker/python/Dockerfile.dev**: We will use a development container with all the tools needed to run the project also with the tool to debug.
