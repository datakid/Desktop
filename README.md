# Lx Workspace

Window manager, command palette and dock for seven tools, in the browser. Each tool opens in its own window.

## What it does

- Opens the tools Form, Dashboard, Compare, Files, Protocols, List and Calculator in windows that can be moved, snapped, minimised, maximised and closed.
- Opens a tool in a new window, adds it as a tab to the current window, or opens it in the browser skipping the preview.
- Searches apps and commands with Ctrl+K. Alt+1 to Alt+7 open the tools, Ctrl+Enter opens a new window, Ctrl+Shift+Enter adds a tab, Alt+Enter opens in the browser, Alt+W closes a window, Ctrl+Shift+L toggles the theme and Ctrl+/ lists the shortcuts.
- Settings: system, light or dark theme, accent colour, three wallpapers, a 12-hour clock, reduce transparency, reduce motion, and a workspace reset.
- Keeps the layout and settings in `localStorage` under `lxos`.

## What it does not do

- It does not contain the tools. Each window frames the tool's own site, so a site that refuses to be framed can only be opened in the browser.
- The list of seven tools is fixed in `index.html`.
- It has no accounts or sync.

## Network and install

Calls each tool's own site when its window opens, and nothing else. It loads no fonts or libraries. Installable (PWA); works offline after the first load, except for the tools themselves.

## Built with

One HTML file, a web manifest and a service worker. There is no build step, no framework and no libraries.

## Run locally

Serve the folder with any static file server. The service worker needs an origin, so opening `index.html` from disk does not register it.
