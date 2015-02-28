# FoundationDB Client Docker Image

[![Docker Repository on Quay.io](https://quay.io/repository/ripple/fdb-client/status "Docker Repository on Quay.io")](https://quay.io/repository/ripple/fdb-client)

Based on Mike McMahon's [excellent scripts](https://bitbucket.org/mmcm/sql-layer-docker). Modified to follow official Docker images' practices more closely by [Peter Petrov](https://github.com/pesho/docker-fdb). This repository is maintained by the folks at [Ripple Labs](https://ripplelabs.com).

# Usage

This image can be used directly as a way to get access to the `fdbcli` utility.

``` sh
# Run a FoundationDB Server
docker run -d --name fdb quay.io/ripple/fdb-server

# Connect to it from another container and print the cluster status
docker run --rm --volumes-from fdb quay.io/ripple/fdb-client fdbcli --exec "status details"
```

You can also run fdbcli in interactive mode:

``` sh
docker run -it --rm --volumes-from fdb quay.io/ripple/fdb-client fdbcli
```

# Related Images

| Image | [GitHub](https://github.com) | [Quay.io](https://quay.io) |
| ----- | ------ | ------- |
| FoundationDB Server | [ripple/docker-fdb-server](https://github.com/ripple/docker-fdb-server) | [![Docker Repository on Quay.io](https://quay.io/repository/ripple/fdb-server/status "Docker Repository on Quay.io")](https://quay.io/repository/ripple/fdb-server) |
| FoundationDB Client | [ripple/docker-fdb-client](https://github.com/ripple/docker-fdb-client) | [![Docker Repository on Quay.io](https://quay.io/repository/ripple/fdb-client/status "Docker Repository on Quay.io")](https://quay.io/repository/ripple/fdb-client) |
