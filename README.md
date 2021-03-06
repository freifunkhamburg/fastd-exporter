# fastd-exporter

We are building a prometheus exporter for the [fastd](https://projects.universe-factory.net/projects/fastd/wiki) vpn daemon.

We have a working version, but the metrics, and by extension their labels, are not stable yet.
When they are we will very likely be tagging our first release.

## Getting Started

For now run

```
$ go get github.com/freifunk-darmstadt/fastd-exporter
```

and

```
$ ./fastd-exporter --instance ffda --metrics.perpeer
```

The exporter will need read access to both the instances `fastd.conf` and `status socket`, keep that in mind.

By default the metrics webserver will listen on `:9281`, which can be changed through the `--web.listen-address` parameter.

Check out the help for additional information.

```
$ ./fastd-exporter --help
```

## Development

We are happy to discuss the fastd-exporter with you on:

> irc.hackint.org #fastd-exporter

### Formatting

We are using go's internal formatting for this codebase.

```
$ go fmt
```
