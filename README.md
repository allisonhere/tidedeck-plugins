# TideDeck plugins

Plugins for [TideDeck](https://github.com/allisonhere/tidedeck), a terminal
dashboard.

## Install

In TideDeck: settings (`s`) → **Plugins**, paste a source, press **Install**.

- `https://github.com/allisonhere/tidedeck-plugins#docker` — **Containers**

## docker

Docker containers, their state and health, read from `docker ps`. Type to
filter by name or image; `c` copies the matched container's id; zoom shows the
image, ports, mounts, created time, and command for each container.

Requires `docker` and `jq`.
