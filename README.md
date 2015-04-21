peerflix-server
===============

[![Build Status](https://travis-ci.org/asapach/peerflix-server.svg?branch=master)](https://travis-ci.org/asapach/peerflix-server)

Streaming torrent client for node.js with web ui.

![screen capture](https://cdn.rawgit.com/asapach/peerflix-server/master/capture.gif)

Based on [torrent-stream](https://github.com/mafintosh/torrent-stream), inspired by [peerflix](https://github.com/mafintosh/peerflix).

## Start Peerflix Server now

[![Launch on PeerVM](https://s3-us-west-2.amazonaws.com/peervm/peervm_button.png)](http://peervm.com?run=docker%20run%20-p%209000%3A9000%20hiteck%2Fpf&name=Peerflix%20Server&ref=)

## Usage

1. `npm install -g peerflix-server`
1. `peerflix-server`
1. Open your browser at [http://localhost:9000/](http://localhost:9000/)
1. Enjoy!

## Configuration

You can configure the application using `~/.config/peerflix-server/config.json` file (doesn't exist by default). The [options](https://github.com/mafintosh/torrent-stream#full-api) are passed to all torrent-stream instances. Here's an example that overrides the defaults:

```json
{
  "connections": 50,
  "tmp": "/mnt/torrents"
}
```

The application stores its current state (list of torrents) in `~/.config/peerflix-server/torrents.json`

## Daemon

If you want to run peerflix-server as a daemon, you can do it using [forever](https://github.com/nodejitsu/forever):

`npm install -g forever`

`forever start /usr/local/bin/peerflix-server` (the path depends on your distribution and npm configuration)

You might also want to enable logging -- see the [docs](https://github.com/nodejitsu/forever#using-forever-from-the-command-line).

## Development

See [Development.md](./Development.md)

## REST API

See [REST.md](./REST.md)
