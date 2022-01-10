# immutable-x-openapi

This contains an *unofficial* OpenAPI 3.0 definitions for 

- the [Immutable X APIs](https://docs.x.immutable.com/reference)
- the [Gods Unchained APIs](https://github.com/immutable/gods-unchained-api)

The definitions were created using [Stoplight Studio](https://stoplight.io/studio/).

You can use the definition to [generate your own SDK](https://openapi.tools/), or import into your favorite
API client such as [Insomnia](https://insomnia.rest/) and [Postman](https://www.postman.com/).

![](assets/insomnia.png)

## Building an SDK: javascript / node.js example

You can use the [openapi-typescript-codegen](https://www.npmjs.com/package/openapi-typescript-codegen) package to 
build an SDK complete with Typescript definitions to make requests to the APIs.

If you copy the appropriate `reference/*.yaml` file to your project and install `openapi-typescript-codegen`,
you can generate the SDK using a `script` command in your `package.json`:

```json
{
  "scripts": {
    "gu-client:build": "openapi --input GodsUnchained-API-OpenAPI3.yaml --useOptions --output ./src/gu-api-client"
  }
}
```

## Notes

These definitions were crafted by hand using the available documentation.

Although a best effort was made to ensure accuracy in results, there may be mistakes in the definition. If you find
such a mistake, please open a pull request with the necessary changes.

For many endpoints, model definitions have been created for responses, which a code generator can use to create
corresponding classes, or typed interfaces if using a Typescript generator.

## Undocumented APIs

### Immutable X

The following endpoints were unable to be documented at the time due to unavailability of the documentation:

- https://docs.x.immutable.com/reference/post_v1-signable-deposit-details-1
- https://docs.x.immutable.com/reference/post_v1-signable-order-details-1
- https://docs.x.immutable.com/reference/post_v1-signable-transfer-details-1
- https://docs.x.immutable.com/reference/post_v1-signable-withdrawal-details-1

## Contributing

- Fork this repo
- Use Stoplight Studio to open the repo directory, and make your edits
- Make sure the linter in Stoplight Studio has no errors/warnings
- Make a pull request with your changes

## Disclaimer

The API definitions depend on the community to keep up-to-date, or until the Immutable team
provides an official definition. Use at your own risk, not responsible for losses incurred from an incorrect
API definition.
