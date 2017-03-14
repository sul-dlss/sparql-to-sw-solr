[![Build Status](https://travis-ci.org/sul-dlss/sparql-to-sw-solr.svg?branch=master)](https://travis-ci.org/sul-dlss/sparql-to-sw-solr)
[![Coverage Status](https://coveralls.io/repos/github/sul-dlss/sparql-to-sw-solr/badge.svg)](https://coveralls.io/github/sul-dlss/sparql-to-sw-solr)
[![Dependency Status](https://gemnasium.com/badges/github.com/sul-dlss/sparql-to-sw-solr.svg)](https://gemnasium.com/github.com/sul-dlss/sparql-to-sw-solr)

[![GitHub version](https://badge.fury.io/gh/sul-dlss%2Fsparql-to-sw-solr.svg)](https://badge.fury.io/gh/sul-dlss%2Fsparql-to-sw-solr)

# sparql-to-sw-solr

Perform SPARQL queries against a triplestore to get the data to create Solr documents specific to SearchWorks ... and write the Solr documents to Solr.

## Development

### Installing code locally

```
bundle
```

### Running tests locally

```
rake spec
```


## Deployment

Capistrano is used for deployment.

1. On your laptop, run

    `bundle`

  to install the Ruby capistrano gems and other dependencies for deployment.

2. Set up shared directories on the remote VM:

    ```
    ssh remote-vm
    cd sparql-to-sw-solr
    mkdir shared
    mkdir shared/log
    ```

3. Deploy code to remote VM:

    `cap dev deploy`


### Running Code Remotely

Code is run as a batch process via Capistrano.
