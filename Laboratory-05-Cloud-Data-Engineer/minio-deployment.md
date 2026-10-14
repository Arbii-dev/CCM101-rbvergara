
# MinIO Technical Documentation

## Overview

This document describes how I deployed a MinIO object storage server using Docker in a KillerCoda Ubuntu Playground, accessed its web console, and created a bucket.

## 1. Docker Command Used

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  scnd/minio-mirror:RELEASE.2025-09-07T16-13-09Z server /data --console-address ":9001"
```

### Note on the image used

The activity sheet specifies `minio/minio`. When I ran it, Docker returned `pull access denied for minio/minio`, because MinIO removed its images from Docker Hub in September 2026. The alternative `quay.io/minio/minio` also failed with an `unauthorized` error, because Quay now blocks anonymous pulls.

I used `scnd/minio-mirror`, a third-party mirror that describes itself as an unmodified copy of the last official MinIO image. It uses the same startup command and options as the original. This is suitable for a lab environment only, not for actual data.

### What each part of the command does

| Part | Purpose |
|------|---------|
| `docker run -d` | Creates and starts a container in detached (background) mode |
| `-p 9000:9000` | Maps
