# satellite-json-server

![LGTM](https://i.lgtm.fun/2p13.png)

### RUN
```
$ npx json-server db.
json
JSON Server started on PORT :3000
Press CTRL-C to stop
Watching db.json...

( ˶ˆ ᗜ ˆ˵ )

Index:
http://localhost:3000/

Static files:
Serving ./public directory if it exists

Endpoints:
http://localhost:3000/posts
http://localhost:3000/comments
http://localhost:3000/profile
```
### Launch
- ⚠️ Do you want to tweak these settings before proceeding? Yes
```
$ flyctl launch
An existing fly.toml file was found for app satellite-json-server
? Would you like to copy its configuration to the new app? No
Scanning source code
Detected a Dockerfile app
Creating app in /home/nori/code/satellite-json-server
We're about to launch your app on Fly.io. Here's what you're getting:

Organization: data.mario24@gmail.com (fly launch defaults to the personal org)
Name:         satellite-json-server  (derived from your directory name)
Region:       Tokyo, Japan           (this is the fastest region for you)
App Machines: shared-cpu-1x, 1GB RAM (most apps need about 1GB of RAM)
Postgres:     <none>                 (not requested)
Redis:        <none>                 (not requested)

? Do you want to tweak these settings before proceeding? Yes
failed opening browser. Copy the url (https://fly.io/cli/launch/686ae10db106f7695540577746dc19d2) into a browser and continue
Waiting for launch data... Done
Created app 'satellite-json-server' in organization 'personal'
Admin URL: https://fly.io/apps/satellite-json-server
Hostname: satellite-json-server.fly.dev
Wrote config file fly.toml
Validating /home/nori/code/satellite-json-server/fly.toml
Platform: machines
✓ Configuration is valid
==> Building image
Remote builder fly-builder-polished-rain-5752 ready
Remote builder fly-builder-polished-rain-5752 ready
==> Building image with Docker
--> docker host: 20.10.12 linux x86_64
[+] Building 2.1s (10/10) FINISHED
 => [internal] load build definition from Dockerfile               0.3s
 => => transferring dockerfile: 32B                                0.3s
 => [internal] load .dockerignore                                  0.3s
 => => transferring context: 34B                                   0.3s
 => [internal] load metadata for docker.io/library/node:20.11      1.3s
 => [1/5] FROM docker.io/library/node:20.11@sha256:fd0115473b2934  0.0s
 => [internal] load build context                                  0.3s
 => => transferring context: 29B                                   0.3s
 => CACHED [2/5] WORKDIR /app                                      0.0s
 => CACHED [3/5] RUN npm install -g npm                            0.0s
 => CACHED [4/5] RUN npm install -g json-server                    0.0s
 => CACHED [5/5] COPY ./db.json /app                               0.0s
 => exporting to image                                             0.0s
 => => exporting layers                                            0.0s
 => => writing image sha256:2198c7c3d56f532edac8aaf257f684c8d08fe  0.0s
 => => naming to registry.fly.io/satellite-json-server:deployment  0.0s
--> Building image done
==> Pushing image to fly
The push refers to repository [registry.fly.io/satellite-json-server]
b564424c2eb0: Pushed
4f89fab74e2b: Pushed
17e097280771: Pushed
31e8a418105c: Pushed
f6780a659019: Pushed
b0445205348c: Pushing [==================================================>]  7.541MB
91d97cac4f7c: Pushing [===========>                                       ]  37.32MB/160.6MB
e27cf0956124: Pushed
d43f876e6f21: Waiting
9f843c569746: Waiting
bcd354c940e1: Waiting
```

### DEPLY
```sh
$ fly deploy
```

### FROM
- https://www.npmjs.com/package/json-server
