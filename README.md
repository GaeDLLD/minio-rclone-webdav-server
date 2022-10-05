# minio-rclone-webdav-server

A @rclone served WebDAV server with @minio as the s3 storage backend docker example

![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/toby1991/rclone-webdav.svg)

## Run
```bash
git clone https://github.com/gaedlld/minio-rclone-webdav-server
cd minio-rclone-webdav-server
docker-compose up -d
```

Then use your favorite WebDAV connect:
* Host: `http://127.0.0.1:80`
* Username: `admin`
* Password: `password`

## Env Configuration
> Your Minio Bucket Name
```
BUCKET: test-bucket 
```
> Your Webdav basic-auth username
```
AUTH_USER: admin
```
> Your Webdav basic-auth password
```
AUTH_PASS: password
```
> Your Webdav access base path, default "/", usually used for Webdav behind nginx/traefik
```
BASE_URL: /
```
> Your Rclone WebGUI username
```
RC_USER: admin
```
> Your Rclone WebGUI password
```
RC_PASS: password
```

## Dashboard
* Host: `http://127.0.0.1:5572`
* Username: `admin`
* Password: `password`

## Fuse
add `--cap-add SYS_ADMIN --device /dev/fuse --security-opt apparmor:unconfine` when running.
