# p4pa-email-templates

This repo contains the mail template(s) override sent on behalf of PU based on the broker involved.

Documents are organized according to the following folder structure:
* <BROKER_EXTERNAL_ID>
    * <EMAIL_TEMPLATE_NAME>
        * index.html
        * index.mjml
        * attachments.txt

Templates are created using [MJML](https://mjml.io/) markup language along with typescript files.

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
