# Shadhini Jayatilake | Personal Website

## Local setup using Docker

```bash
docker compose pull
docker compose up
```

**Note**

- When you run it for the first time, it will download a docker image of size 400MB or so.
- To see the template running, open your browser and go to http://localhost:8080.

### To use the slimmed docker image with a size below 100MBs and exact same functionality

```bash
docker compose -f docker-compose-slim.yml up
```

### Build your own docker image

- Necessary, if you would like to build an older or very custom version of al-folio

```bash
docker compose up --build
```

- Builds or rebuilds the services defined in your docker-compose.yml file.
- It forces the rebuild of images for all services before starting the containers.
- If an image already exists locally, it will be rebuilt.

* If you want to update jekyll, install new ruby packages, etc.,
  - build the image again using `--force-recreate` argument at the end of the previous command! 
  - It will download Ruby and Jekyll and install all Ruby packages again from scratch.

* If you want to use a specific docker version
  - changing latest tag to your_version in `docker-compose.yaml`
  - E.g: you might have created your website on v0.10.0 and you want to stick with that.

## Deployment

Make changes to the main/master branch, commit, and push!
