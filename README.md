# Node-todo

[![Blimp demo badge](https://kelda.io/demo-badge.svg?repo=https://github.com/kelda/node-todo.git)](https://kelda.io/preview-env/?repo=https://github.com/kelda/node-todo.git&port=web:8080)

This repo contains an example `node` application that stores data in
`mongo`. Shout out to the original author,
[scotch-io](https://github.com/scotch-io/node-todo).

## Local development with Blimp

The following instructions will walk you through using `blimp` to develop in
the cloud.

### 1. Clone this repo

```
git clone https://github.com/kelda-inc/node-todo
```

### 2. Download Blimp

```
curl -fsSL 'https://kelda.io/install-blimp.sh' | sh
```

### 3. Login

This creates an isolated sandbox that your Docker containers will run in.

```
blimp login
```

### 4. Boot the app

```
blimp up
```

This will boot the `node` and `mongo` containers. Once they're up, access the
todo UI at [http://localhost:8080](http://localhost:8080), and a couple todo tasks.

If you have `docker` installed locally, and want to try the image building
feature, run `blimp up -f ./docker-compose-local-build.yml` instead.

### 5. Make a code change

Open `app/routes.js` in your preferred text editor, uncomment the code on line
12, and save the file.

Kelda Blimp will sync the change into the container, and `nodemon` will restart
the Node server.

### 6. Confirm that the code change worked

Reload [http://localhost:8080](http://localhost:8080). You will now see each
todo prepended with "Kelda:"

### 7. Explore the other Blimp commands

```
blimp ps

blimp logs web

blimp ssh web
```

## Demo environment

[Boot a personal demo copy of
node-todo](https://kelda.io/preview-env/?repo=https://github.com/kelda/node-todo.git&port=web:8080)
from your browser without downloading or setting up anything.

Clicking the
[link](https://kelda.io/preview-env/?repo=https://github.com/kelda/node-todo.git&port=web:8080)
boots this repo in the Blimp cloud, and creates a public URL for you to access
it.
