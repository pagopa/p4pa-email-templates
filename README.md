# p4pa-email-templates

This repo contains the mail template(s) override sent on behalf of PU based on the broker involved.

Documents are organized according to the following folder structure:
* <BROKER_EXTERNAL_ID>
    * partials (folder) 
    * <EMAIL_TEMPLATE_NAME>
        * index.html
        * index.mjml
        * attachments.txt
        * attachments (folder)
        * partials (folder)

Put inside attachments folder all the files referenced in attchments.txt file.

Put inside partials folder all reusable .mjml templates:
* for partials at <EMAIL_TEMPLATE_NAME> level, in CLI command only need to add option: --config.allowIncludes true
* for partials at <BROKER_EXTERNAL_ID> level, in CLI command need to add both options: --config.allowIncludes true --config.includePath <PARTIALS_PATH> 

Templates are created using [MJML](https://mjml.io/) markup language along with typescript files.

## Use cases

See [Confluence Page](https://pagopa.atlassian.net/wiki/spaces/SPAC/pages/2916581443/Invio+Email)

## How to apply changes

To edit them, you can choose among these following options:

- [Online editor](https://mjml.io/try-it-live)
- [Local installation](https://mjml.io/download)
- [Visual Studio Code plugin](https://marketplace.visualstudio.com/items?itemName=mjmlio.vscode-mjml)

To generate the HTML output you need to install the following CLI tool:

1. [MJML](https://www.npmjs.com/package/mjml) package:

```shell
npm install -g mjml && mjml <MJML_INPUT_FILE> -o <OUTPUT_FILE> [--config.allowIncludes true --config.includePath <BROKER_PARTIALS_PATH>]
```

Example:

npm install -g mjml && mjml cie/INGESTION_PAGOPA_RT/index.mjml -o cie/INGESTION_PAGOPA_RT/index.html --config.allowIncludes true --config.includePath cie/partials
