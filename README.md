# Estuary

> An experimental ipfs node

## Building

Requirements:
- go (1.15 or higher)

1. Clone and build the lotus codebase adjacent to this repo (so that its at `../lotus`)
  - `git clone https://github.com/filecoin-project/lotus`
2. Run `go build`

## Running

To run locally in a 'dev' environment, first run:
```
./estuary setup
```

Save the auth token that this outputs, you will need it for interacting with
and controlling the node.

NOTE: if you want to use a different database than a sqlite instance stored in your local directory, you will need to configure that with the `--database` flag, passed before the setup command: `./estuary --database=XXXXX setup`

Once you have the setup complete, choose an appropriate directory for estuary to keep its data, and use it as your datadir flag when running estuary.
You will also need to tell estuary where it can access a lotus gateway api, we recommend using:
```
export FULLNODE_API_INFO=wss://api.chain.love
```

Then run:

```
./estuary --datadir=/path/to/storage --database=IF-YOU-NEED-THIS --logging
```


