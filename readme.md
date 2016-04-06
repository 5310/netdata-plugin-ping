# netdata-plugin-ping

A Node.js external plugin for [Netdata](https://github.com/firehol/netdata) that logs pings.

## Installation

1. Install the NPM package globally.
  - `npm install -g 5310/netdata-plugin-ping`
2. Symlink the script to the Netdata plugins directory (`/usr/libexec/netdata/plugins.d/` by default).
  - `ln -s /usr/lib/node_modules/netdata-plugin-ping/ping.plugin /usr/libexec/netdata/plugins.d/ping.plugin`
3. Enable the plugin by editing Netdata configurations (`/etc/netdata/netdata.conf` by default) and adding `ping = yes` under the `[plugins]` section.

## Usage

The plugin accepts the standard update-interval value as the first argument in the command line, and any additional arguments will be interpreted as domain names to ping, overriding the default (8.8.8.8).

 E.g: `ping.plugin 10 google.com github.com` will ping Google and GitHub every ten seconds.

Custom update intervals and domains can likewise be specified in the Netdata configurations.
