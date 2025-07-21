# Jstz Web API Support

Quick and dirty audit of Web API support in Jstz. See <https://jstz-dev.github.io/nodejs-compat-matrix/>.

The report displayed is a truncated version of the [upstream report](https://workers-nodejs-compat-matrix.pages.dev). All Node.js APIs are removed because Jstz does not support Node.js APIs at all.

## Install

Get [pnpm](https://pnpm.io/installation) and then

```shell
pnpm install
```

## Generate the table

Here all individual reports are assumed to be up-to-date. To update them, update the `dev` branch with upstream and then merge `dev` into `deploy`.

> [!IMPORTANT]
> It's not recommended to update the individual reports locally as somehow the results are not consistent. Take the upstream repository as the source of truth.

> [!IMPORTANT]
> This requires features from Node v22, so if it isn't your default node version, run `nvm use 22` and proceed.

### Work with Jstz dev locally

* Run the `api_coverage` test in [jstz_runtime](https://github.com/jstz-dev/jstz/tree/main/crates/jstz_runtime).
* Copy the output report to `data/jstz.json`.

### Generate the table

  ```shell
  pnpm run generate:table
  ```

## Serve a local version of the report

```shell
pnpm run report:dev
```
