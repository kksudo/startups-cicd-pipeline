## python/

It's a submodule of the most popular '[Full Stack FastAPI Template](https://github.com/tiangolo/full-stack-fastapi-template/tree/master/backend)' git repository. In this case we focus only on the backend part of the project.

In spite of the fact that the project already have automation we will create a new one to make the deployment process easier to use best practices.

### Differences from the original project

- **Dockerfile**: We will use a production ready slim container with only application(without migrations, tests, etc).
- **Dockerfile.full**: We will use a development container with all dependencies like tests, migrations, etc.
- **Dockerfile.dev**: We will use a development container with all the tools needed to run the project also with the tool to debug.
