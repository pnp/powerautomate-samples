# Power Automate Samples

This folder contains one sample Power Automate flow per folder.

## Submitting a sample

Create the sample-root `README.md` from [README-template.md](README-template.md). Its final line must be:

```html
<img src="https://m365-visitor-stats.azurewebsites.net/powerautomate-samples/{sample-path}" />
```

Replace `{sample-path}` with the sample folder's repository-relative path. For example, a sample stored in `samples/my-sample` must use:

```html
<img src="https://m365-visitor-stats.azurewebsites.net/powerautomate-samples/samples/my-sample" />
```

Catalog metadata belongs at `assets/sample.json` within the sample folder and must reference the [PnP sample metadata schema](https://developer.microsoft.com/en-us/json-schemas/pnp/samples/v1.0/metadata-schema.json). The catalog workflow reads metadata only from that location. Keep its title, descriptions, sample URL, products, tags, authors, and references aligned with the sample-root `README.md`.
