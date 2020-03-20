# Try out Kelda Blimp

This directory contains an example `node` application that stores data in
`mongo`. Shout out to the original author,
[scotch-io](https://github.com/scotch-io/node-todo).

The following instructions will walk you through using `blimp` to develop in
the cloud.

## 1. Download Kelda Blimp

```
curl -fsSL 'https://kelda.io/install-blimp.sh' | sh
```

## 2. Login to Kelda Blimp

This creates an isolated sandbox that your Docker containers will run in.

```
blimp login
```

## 2. Boot the app

```
blimp up
```

This will boot the `node` and `mongo` containers. Once they're up, access the
todo UI at [http://localhost:8080](http://localhost:8080).

## 3. Explore the other Blimp commands

```
blimp ps

blimp logs web

blimp ssh web
```
