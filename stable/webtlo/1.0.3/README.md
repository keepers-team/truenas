# Introduction

![Version: 1.0.3](https://img.shields.io/badge/Version-1.0.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.9.9](https://img.shields.io/badge/AppVersion-2.9.9-informational?style=flat-square)

Torrent management for keepers

This app is designed to be installed as TrueNAS SCALE app only. We can not guarantee this charts works as a stand-alone helm installation.

## Source Code

* <https://github.com/keepers-team/truenas/tree/main/stable/webtlo>
* <https://github.com/keepers-team/webtlo>
* <https://hub.docker.com/r/berkut174/webtlo>

## Requirements

Kubernetes: `>=1.16.0-0`

## Dependencies

| Repository | Name | Version |
|------------|------|---------|
| https://library-charts.truecharts.org | common | 10.6.11 |

## Installing the Chart

To install this Chart on TrueNAS SCALE:

* Make sure your storage-pool is created and working
* Make sure you have a working internet connection and can reach `github.com` from the host system.

### Adding catalog

When opening the Apps menu item on TrueNAS SCALE for the first time, you get prompted to setup a new pool for Apps. This will create a new dataset on the
selected pool called "ix-applications", which will contain all docker containers and most application data, unless specified otherwise.

* Go to "Apps" in the left hand menu
* Select the "Manage Catalogs" tab
* Click "Add Catalog" and enter the required information:
* Name: `keepers`
* Repository: `https://github.com/keepers-team/truenas.git`
* Preferred Trains: `stable`
* Branch: `main`

### Install
Just search for `webtlo` application. For convenience refer to [Installing an App Guide] from TrueCharts.

## Uninstall

To upgrade, rollback or delete this Chart from TrueNAS SCALE check TrueChart's [Quick-Start Guide]

## Configuration

### Available Settings

Read through the `values.yaml` file. It has several commented out suggested values.
Other values may be used from the [values.yaml], and the [common library].

## Connecting to other charts

If you need to connect this Chart to other Charts on TrueNAS SCALE, like torrent-client or so, please refer to TrueCharts' [Linking Charts Internally]
quick-start guide.

## Support

- See the [Wiki](https://webtlo.keepers.tech)
- Open a [issue](https://github.com/keepers-team/truenas/issues/new/choose)

[Linking Charts Internally]: https://truecharts.org/docs/manual/SCALE%20Apps/linking-apps

[values.yaml]: https://github.com/truecharts/library-charts/tree/main/charts/stable/common/values.yaml

[common library]: https://github.com/k8s-at-home/library-charts/tree/main/charts/stable/common

[Quick-Start Guide]: https://truecharts.org/docs/manual/SCALE%20Apps/Upgrade-rollback-delete-an-App

[Installing an App Guide]: https://truecharts.org/docs/manual/SCALE%20Apps/Installing-an-App
