# Contributing 

We love community contributions! Help us expand this project with your configured collector templates.

Have an idea, but don't know where to start? Open an issue and we'll help you!

## Project Structure

Configurations must be stored in a logical structure:

```text
processors/
  <vendor>/
    <product>/
      README.md
      <processor_id>.json
      samples/
        <sample1>.json
        <sample2>.json
        ...
```

`<vendor>` is a normalized form of the vendor's name, for example: `Palo Alto Networks` to `panw`, or when there is no specific vendor use a descriptive like `linux` for linux os logs

`<product>` is a normalized form of the vendor's product name, for example: `Cortex XDR` to `cortex_xdr`

`<processor_id>` is a simple descriptive name for the collector template.

## Standards

Each template directory must include a README file with a minimum set of details:

1. The author of the Template and any relevant contact information
2. A description of what the template does and the expected behavior and outcome of the template, including volume reduction percentage
3. Any changes required to the template to ensure it functions correctly

A sample of events that work in the processor is required for merge approval


## Sample Data

Any sample data included with the template must be placed into the `samples` directory, and have a descriptive name.

⚠️ Absolutely no sensitive data should be committed to this repo! You are responsible for ensure the complete sanitization of any submitted samples.

## Recommendations

It is recommended that you pretty print your JSON templates before opening your pull request. a great tool for this is [jsonformatter.org](jsonformatter.org).