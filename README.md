# FileFlows for TOS 7 (Docker)

自动化的媒体文件处理流水线。按自定义规则对视频和音频转码、重封装、补充或替换音轨、提取字幕并整理媒体库，处理流程与任务队列通过浏览器管理。

An automated media processing pipeline. Transcode, remux, add or replace audio tracks, extract subtitles and organize your library with custom rules, managed from a browser.

## Package

- Application ID: `fileflows`
- Type: Docker (TOS 7)
- Architecture: `x86_64`, `aarch64`
- Upstream image: see `docker-compose.yml` in the downloaded asset
- Web UI port: declared in `x-app-meta`

## Source

The `src/` directory contains the files the package is built from:

- `src/config.x86_64.ini` / `src/config.aarch64.ini` — `config.ini` per architecture
- `src/docker-compose.yml` — compose template; `@@...@@` placeholders are replaced at build time
- `src/fileflows.lang` — 14 language sections
- `src/fileflows.svg` — application icon

Build toolchain: https://github.com/Irvingfei/docker-apps

## Install

1. In the TOS App Center, add this repository's application and submit the matching `fileflows_<arch>.tar.gz` asset from the latest Release.
2. Data is stored under `/Volume<N>/DockerAppData/fileflows/` through the compose bind mounts.

## Notes

数据保存在应用数据目录的 data、logs 与 temp 子目录中，卸载时只有勾选删除数据才会清理。

This repository packages the upstream open-source application for TerraMaster TOS 7.
It is not affiliated with or endorsed by the upstream project. Application names and
trademarks belong to their respective owners. All images are pulled from Docker Hub.
