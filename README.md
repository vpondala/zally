# Zally: A Minimalistic, Simple-to-Use API Linter

[![Build Status](https://travis-ci.org/zalando-incubator/zally.svg?branch=master)](https://travis-ci.org/zalando-incubator/zally)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/05a7515011504c06b1cb35ede27ac7d4)](https://www.codacy.com/app/zally/zally?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=zalando-incubator/zally&amp;utm_campaign=Badge_Grade)
[![Codacy Badge](https://api.codacy.com/project/badge/Coverage/05a7515011504c06b1cb35ede27ac7d4)](https://www.codacy.com/app/zally/zally?utm_source=github.com&utm_medium=referral&utm_content=zalando-incubator/zally&utm_campaign=Badge_Coverage)

<p align="center">
  <img src="logo.png" width="200" height="200" />
</p>

Zally is a quality assurance tool for OpenAPI specifications. It helps you to check your APIs for compliance with a set of rules and best practices. Zally comes with a default set of rules that checks for compliance with the [Zalando RESTful API and Event Scheme Guidelines](https://zalando.github.io/restful-api-guidelines/).

Zally is designed to be easy to use and to integrate into your existing development workflow. You can use Zally as a command-line tool, a web-based UI, or as a part of your CI/CD pipeline.

## Features

* **Rich set of Rules:** Zally comes with a rich set of rules to check for compliance with the Zalando RESTful API and Event Scheme Guidelines.
* **Easy to use:** Zally comes with a simple and intuitive command-line interface (CLI) and a web-based user interface (UI).
* **Extensible:** You can easily create your own custom rules to enforce your own API guidelines. Zally is written in Kotlin, which makes it easy to write new rules.
* **Integrates with your workflow:** Zally can be integrated with your existing CI/CD pipeline to automatically check your APIs for compliance.
* **Supports OpenAPI 2.0 (Swagger) and 3.0:** Zally can lint both OpenAPI 2.0 and 3.0 specifications.

## Getting Started

### Prerequisites

* [Docker](https://www.docker.com/get-started)
* [Docker Compose](https://docs.docker.com/compose/install/)

### Running Zally

The easiest way to get started with Zally is to use the provided `build-and-run.sh` script. This script will build and run all the components of Zally, including the server, the web UI, and the database.

```bash
./build-and-run.sh
```

Once the script has finished, you can access the web UI at `http://localhost:8080` and the Zally server at `http://localhost:8000`.

### Linting your first file

You can use the Zally CLI to lint an OpenAPI specification. The CLI is available as a pre-compiled binary for Linux, macOS, and Windows. You can download the latest release from the [releases page](https://github.com/zalando/zally/releases).

Once you have downloaded the CLI, you can lint a file using the following command:

```bash
zally lint path/to/your/swagger.yaml
```

## Components

Zally is composed of several components:

* **[Server](server/README.md):** The server is the core of Zally. It provides a REST API for linting OpenAPI specifications.
* **[CLI](cli/README.md):** The command-line interface (CLI) is a tool for interacting with the Zally server from the command line.
* **[Web UI](web-ui/README.md):** The web UI is a user-friendly interface for linting OpenAPI specifications.
* **[GitHub Integration](github-integration/README.md):** Zally can be integrated with GitHub to automatically lint your OpenAPI specifications when you push changes to your repository.

For more information about each component, please refer to the `README.md` file in the corresponding directory.

## Configuration

Zally can be configured using a `zally.yaml` file. This file allows you to enable and disable rules, and to configure the behavior of Zally.

Here is an example of a `zally.yaml` file:

```yaml
rules:
  # Disable the UseStandardHttpStatusCodes rule
  UseStandardHttpStatusCodes: off
```

For more information about the configuration options, please refer to the [Zally documentation](https://zalando.github.io/zally/user-guide/rules).

## Contributing

We welcome contributions from the community. If you would like to contribute to Zally, please read our [contributing guidelines](CONTRIBUTING).

## License

Zally is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
