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

Put inside attachments folder all the files referenced in attchments.txt file.

Put inside partials folder all reusable .mjml templates; if positioned outside template folder, compilation command needs to take its position into account.

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
npm install -g mjml && mjml <MJML_INPUT_FILE> -o <OUTPUT_FILE> [--config.allowIncludes true]
```
