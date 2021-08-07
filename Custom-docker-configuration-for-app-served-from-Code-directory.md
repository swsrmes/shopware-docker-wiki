Shopware docker detects automatically for your Shopware / Symfony application and provides complete images for any PHP version. Sometimes it is necessary to add a custom docker image like when a Shopware App server is written in another language. To archive this you can override in your project the docker configuration.

To override it create a `.swdc/service.yml` in your project folder in your code directory. The content of this file will be appended to the service definition. Here is an example file:

```yaml
image: my-app
environment:
  # The domain where it should be available
  # See https://github.com/nginx-proxy/nginx-proxy for all options
  VIRTUAL_HOST: my-app.dev.localhost
# Default docker-compose build a docker image of that path
build:
  context: ~/Code/random-go-app/
```

On next run `swdc up` will take this configuration and run that. Tip: You can use `swdc up --build` to let the build step rebuilt always