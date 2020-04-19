# nci scheduler

Periodic build runner for nci [nci](https://github.com/node-ci/nci).

[![Npm version](https://img.shields.io/npm/v/nci-scheduler.svg)](https://www.npmjs.org/package/nci-scheduler)
[![Known Vulnerabilities](https://snyk.io/test/npm/nci-scheduler/badge.svg)](https://snyk.io/test/npm/nci-scheduler)


## Installation

```sh
npm install nci-scheduler
```


## Usage

To enable add this plugin to the `plugins` section at server config:

```json
{
    "plugins": [
        "nci-scheduler"
    ]
....
}
```

after that you can set scheduler settings at project config e.g. (for building
project every 5 seconds):

```json
    "buildEvery": {
        "time": "*/5 * * * * *",
        "withScmChangesOnly": true
    }
```

parameters:

 - `time` - 6 or 5 (seconds can be omitted) groups cron string
 - `withScmChangesOnly` - if true then build will be started only if there is
scm changes for project
 - `buildParams` - params for the build (override project config)
