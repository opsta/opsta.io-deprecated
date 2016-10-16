Template Scaffolding
============================

Template scaffolding for themes developer include:
* [BrowserSync][browsersync] - auto reload all browser that open development site
* SASS

### Setup
1. npm install
2. `php -S localhost:8889`
3. open new tab and run `grunt`
4. cheer!!

### Setup with Docker

```bash
docker run --rm --workdir /app -v $(pwd):/app node:6.8.0 npm install
docker run -it --rm --workdir /app -v $(pwd):/app -p 8889:8889 php:7.0.12-alpine php -S 0.0.0.0:8889
docker run -it --rm --workdir /app -v $(pwd):/app -p 3000:3000 -p 3001:3001 node:6.8.0 node_modules/grunt-cli/bin/grunt
# Open http://localhost:3000 or http://localhost:3001
```

[browsersync]: http://www.browsersync.io
