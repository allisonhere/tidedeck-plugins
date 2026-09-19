# TideDeck plugins

Plugins for [TideDeck](https://github.com/allisonhere/tidedeck), a terminal
dashboard.

## Install

In TideDeck: settings (`s`) → **Plugins**, paste a source, press **Install**.

- `https://github.com/allisonhere/tidedeck-plugins#ai-usage` — **AI Usage**
- `https://github.com/allisonhere/tidedeck-plugins#docker` — **Containers**
- `https://github.com/allisonhere/tidedeck-plugins#favourites` — **Favourites**
- `https://github.com/allisonhere/tidedeck-plugins#mail` — **Mail**

An installed plugin starts hidden, so its program does not run until its panel is
enabled from the panel picker (`w`, space toggles). The directories here are the
same plugins that ship in TideDeck's `contrib/`, published so they can be
installed and updated without waiting for an app release.

## ai-usage

AI plan usage and balances, one row per account: the plan, how much of it is used
as a gauge, and when it resets. Reads `ai-usagebar usage --json`; the binary is a
setting for when it is not on your `PATH`.

Requires `ai-usagebar` and `jq`.

## docker

Docker containers, their state and health, read from `docker ps`. Type to filter
by name or image; `c` copies the matched container's id; zoom shows the image,
ports, mounts, created time, and command for each container.

Requires `docker` and `jq`.

## favourites

A list of links you keep, and the form that maintains it. `enter` on a row opens
that link in your browser, `e` opens the form for that entry, and the last row -
`＋ add a favourite` - opens a blank form, which is there even when the list is
empty.

Only `http` and `https` links are openable. Anything else is stored, shown and
marked, but never handed to a browser.

The list is one JSON file -
`${XDG_DATA_HOME:-~/.local/share}/tidedeck/favourites.json` unless the `path`
setting says otherwise - so it can be edited by hand as well as by the form.

Requires `xdg-open`.

## mail

A preview of recent mail, read from
[TideMail](https://github.com/allisonhere/tidemail)'s local cache: sender,
subject and age, with unread carried and read muted. `enter` opens the message in
TideMail.

Read-only, and it works while TideMail is closed: it reads the cache, not the
mailbox. No password, no network, nothing running.

Requires TideMail and `jq`.
