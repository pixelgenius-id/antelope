
**NOTICE:**  This was formerly the  @greymass/eosio  library distributed on  [npmjs](https://www.npmjs.com/package/@greymass/eosio)  and also adapted from  [@wharfkit/antelope](https://www.npmjs.com/package/@wharfkit/antelope).

  

Future distributions for Vexanium blockchain will be made using the new organization and namespace, and distributed as @pixelgeniusid/antelope on [npmjs](https://www.npmjs.com/package/@pixelgeniusid/antelope).

  

If you were previously using either  @greymass/eosio  or  @wharfkit/antelope, you can now use  @pixelgeniusid/antelopefor full compatibility with the  **VEXANIUM**  blockchain.

To update your codebase, Remove the @greymass/eosio or @wharfkit/antelope library and add the `@pixelgeniusid/antelope` library, then replace all instances of `@greymass/eosio` and [@wharfkit/antelope](https://www.npmjs.com/package/@wharfkit/antelope) with `@pixelgeniusid/antelope` in all files.

# @pixelgeniusid/antelope

JavaScript library for working with Antelope powered blockchains (formerly EOSIO, still compatible with VEXANIUM).

Avaiable on npm: https://www.npmjs.com/package/@pixelgeniusid/antelope

## Install

```
npm install @pixelgeniusid/antelope
```

## API Documentation

https://pixelgenius-id.github.io/antelope/

## Documentation

Documentation beyond the automatically generated API documentation above is currently incomplete. Until full documentation is complete, the tests themselves provide good reference material on how to do nearly everything.

https://github.com/pixelgenius-id/antelope/tree/master/test

More:

-   Using APIs: https://github.com/pixelgenius-id/antelope/blob/master/test/api.ts
-   Serialization: https://github.com/pixelgenius-id/antelope/blob/master/test/serializer.ts
-   Crypto Operations: https://github.com/pixelgenius-id/antelope/blob/master/test/crypto.ts
-   Primitive Data Types: https://github.com/pixelgenius-id/antelope/blob/master/test/chain.ts

## Reporting Issues

If you think you've found an issue with this codebase, please submit a pull request with a failing unit test to better help us reproduce and understand the issue you are experiencing.

To do this, fork this repository and create your own branch. In this new branch, use the test scaffolding at the path below to write code that either fails to execute, throws an error, or doesn't return the anticipated response.

```
./test/bug-report.ts
```

This specific test can be run within the root project folder either using `make`:

```bash
grep="bug-report" make test
```

Or running `mocha` directly from the installed `./node_modules` folder:

```bash
TS_NODE_PROJECT='./test/tsconfig.json' ./node_modules/.bin/mocha -u tdd -r ts-node/register -r tsconfig-paths/register --extension ts test/*.ts --grep="bug-report"
```

Once your test is failing and successfully shows the issue occurring, please submit a pull request to this repository. Feel free to include any additional details in the body of the pull request that might help us understand the situation.

> NOTE: If you are performing API requests from within unit tests, you will need to prepend `MOCK_RECORD=true` to the above commands in order instruct the test running to execute and cache the API request. Any subsequent API requests will utilize this cache to prevent the test from continously accessing API endpoints. Prefixing your command with `MOCK_RECORD=overwrite` is also possible which forces the test to ignore the cache and fetch new data.

## Running Tests

### Run the unit test suite:

```
make test
```

### Run the unit test suite with coverage:

```
make coverage
```

The report for the current version can also be found at: https://pixelgenius-id.github.io/antelope/coverage/

### Run the test suite in a browser:

```
make browser-test
```

The browser test suite for the current version of the library is available at: https://pixelgenius-id.github.io/antelope/tests.html

## Debugging

Instructions and notes on debugging typescript in your IDE. Explains how to match the Mocha test configuration found in the Makefile.

[Notes on setting up IDE Debuggers](docs/IDE_Debug.md)
