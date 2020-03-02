# Google Cloud Platform-based implementation of _Bifravst :smirk_cat::rainbow:_

[![GitHub Actions](https://github.com/Bifravst/azure/workflows/Test%20and%20Release/badge.svg)](https://github.com/Bifravst/azure/actions)
[![Greenkeeper badge](https://badges.greenkeeper.io/Bifravst/azure.svg)](https://greenkeeper.io/)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier/)
[![ESLint: TypeScript](https://img.shields.io/badge/ESLint-TypeScript-blue.svg)](https://github.com/typescript-eslint/typescript-eslint)

Read the documentation at https://bifravst.github.io/.

## Docker

Build the docker image:

    docker build  -t azure-functions-nodejs-12 .

Export the IotHub connection string (can be found in the function app's
configuration) to the environment variable `IOT_HUB_CONNECTION_STRING`.

Run the functions app:

    docker run --rm --net=host -P -e IOT_HUB_CONNECTION_STRING \
        -v ${PWD}:/workdir azure-functions-nodejs-12:latest \
        func start --typescript
