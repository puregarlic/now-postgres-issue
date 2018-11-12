# Now 2.0 issue with `pg` and `pg-native`

I'm unable to use the Postgres client for NodeJS due to some issues with `@now/node`.

## JS only client

With only the JS client specified in the package.json, the lambda builds
correctly, but errors out on request, as it can't find the `pg-native` module.
I suspect this has something to do with the Rollup build process? From what I
can tell from the `pg` docs, I should be able to use this module without
installing `pg-native` alongside.

> Logs: https://postgres-js-old0worpn.now.sh/_logs

## JS with Native installed

However, when I install `pg-native` alongside `pg`, I encounter a build failure.
It looks like an issue with `node-gyp`, but I don't really know what I can do
about it.

> Logs: https://postgres-js-and-native-q4zdupxq4.now.sh/_logs
