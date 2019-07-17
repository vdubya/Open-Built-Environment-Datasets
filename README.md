[![goodtables.io](https://goodtables.io/badge/github/frictionlessdata/example-data-packages.svg)](https://goodtables.io/github/vdubya/Open-Built-Environmnet-Datasets)

# Open Built Environment Datasets
OBED is a repository for datasets pertaining to the Architecture, Engineering, and Construction (AEC) and other built environment related industries.

1. Data packages must conform to the [Frictionless Data Specification](https://frictionlessdata.io/specs/).
1. Data will be licensed as openly as possible, ideally under the <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
1. CSV data is preferred, but not required.

## Data Packages
A `datapackage.json` file will describe the [data package](https://frictionlessdata.io/specs/data-package/) as a whole, and describe one or more [data resources](https://frictionlessdata.io/specs/data-resource/).

If all the data is tabular (i.e. [CSV files](https://frictionlessdata.io/guides/csv/)), then it will be described as a [tabular data package](https://frictionlessdata.io/specs/tabular-data-package/) with one or more [tabular data resources](https://frictionlessdata.io/specs/tabular-data-package/) each with a [table schema](https://frictionlessdata.io/specs/table-schema/) and, if needed, a [CSV dialect](https://frictionlessdata.io/specs/csv-dialect/).

Each data package is stored in it's own directory:
```
|- data-package-name-1
   |- README.md
   |- datapackage.json
   |- data
      |- data.csv
      |- ...
```
It contains a:
- `README.md` to explain the provenance of the data
- `datapackage.json` a machine readable file that explains the structure and meaning of the data
- one or more data files, typically grouped in a `data` directory

The data package directory may also contain [other files or sub-directories](https://frictionlessdata.io/specs/data-package/#illustrative-structure). These files may be scripts used to prepare the data package or other related resources.

## Templates
A templates directory contains a template [`README.md`](https://github.com/frictionlessdata/example-data-packages/blob/master/templates/README-template.md) and example `datapackage.json` snippets.

### `README.md` template
In this repository, each data package must have a [`README.md`](https://github.com/frictionlessdata/example-data-packages/blob/master/templates/README-template.md). The `README.md` should follow [good practices](https://frictionlessdata.io/guides/publish-faq/#readme).

### `datapackage.json` snippets
JSON snippets provide a fragment of a `datapackage.json` file to help you learn about that specific property or cut and paste into your own data package. E.g. [`licenses.json`](https://github.com/frictionlessdata/example-data-packages/blob/master/templates/licenses.json) could include JSON for each [recommended Open Definition conformant license](http://opendefinition.org/licenses/#conformant-licenses).

## Repository Structure
```
|
|- data-package-name-1
|   |- README.md
|   |- datapackage.json
|   |- data
|     |- data.csv
|     |- data.geojson
|     |- ...
|     
|- data-package-name-2
|  |- etc.
|
|- templates
|  |- README-template.md
|  |- licenses.json
|  |- contributors.json
|  |- dialect.json
|  |- ...
|
|- zip
|  |- data-package-name-1.zip
|  |- data-package-name-2.zip
|
|
|- goodtables.yaml
|- README.md   

```

## Contributing
We value all types of contributions:
- documentation
- data packages
- [issues](https://github.com/frictionlessdata/example-data-packages/issues) and [requests](https://github.com/frictionlessdata/example-data-packages/issues)
- code

We thank the generous [contributors](https://github.com/frictionlessdata/example-data-packages/graphs/contributors) to the Frictionless Data project.

To join them, please read [`CONTRIBUTING.md`](.github/CONTRIBUTING.md) for details on our code of conduct and how to submit a pull request. Each contributed data package should be licensed as openly as possible.

## Zipped Data Packages
With each commit to the repository, the data package directory is converted into a .zip file so it can be used with [software that supports Frictionless Data ](https://frictionlessdata.io/software/) such as the [Data Curator](http://data-curator.io) app or the [DataPackage.js](https://github.com/frictionlessdata/datapackage-js) library. The zip files are stored in the `zip` directory.

While [the Frictionless Data approach to compressing data packages has not been finalised](https://github.com/frictionlessdata/specs/issues/132) a number of [Frictionless Data Software](https://frictionlessdata.io/software/) implementations support zip files.

*To do: script needed*

## Licenses
Data Packages in this project are licensed as specified in each individual `datapackage.json` file. If a license is not specified, it is licensed under the <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>, and this is the preferred (but not required) license for all submitted data.

## Credit
This work is based on the Frictionless Data [Example Data Packages](https://github.com/frictionlessdata/example-data-packages) repository.
