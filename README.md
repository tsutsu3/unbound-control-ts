<a id="readme-top"></a>

> [!CAUTION]
> This project is currently under development

<!-- PROJECT SHIELDS -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[![npm][npm-sheild]][npm-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![CodeCov][codecov-shield]][codecov-url]
[![CodeClimate][codeclimate-shield]][codeclimate-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/tsutsu3/unbound-control-ts">
    <img src="images/Unbound_Outlined_Black.svg" alt="Logo" height="100" >
  </a>

<h3 align="center">unbound-control-ts</h3>

  <p align="center">
    A TypeScript library for configuration and control of Unbound DNS.
    <br />
    <br />
    <a href="https://github.com/tsutsu3/unbound-control-ts">Samples</a>
  </p>
</div>

> [!IMPORTANT]
> **This is an unofficial project, not affiliated with the official Unbound or its maintainers.**

## Table of Contents

1. [About The Project](#about-the-project)
2. [Key Features](#key-features)
3. [Usage](#usage)
   1. [Prerequisites](#prerequisites)
   2. [Install](#install)
   3. [Example Usage](#example-usage)
4. [Development](#development)
   1. [Develop Prerequisites](#develop-prerequisites)
   2. [Develop Setup](#develop-setup)
5. [License](#license)


## About The Project

Unbound is a powerful and versatile DNS resolver that is widely used for enhancing network privacy, security, and performance.

This project provides a TypeScript library designed to simplify interaction with Unbound's unbound-control utility, enabling developers to manage and configure Unbound DNS programmatically with ease.

## Key Features

- **Seamless Integration**: Interact with Unbound directly from your TypeScript or JavaScript projects.
- **User-Friendly API**: A clean and intuitive API for common Unbound operations like querying statistics, reloading configurations, or managing zones.
- **Cross-Platform Compatibility**: Works across various platforms where unbound-control is available.
- **Open Source**: Built with community contributions and extensibility in mind.

Here's a suggestion for the "Usage" section, including installation instructions:

## Usage

### Prerequisites

1. Ensure that `unbound-control` is installed and configured on your system.
2. Make sure the process running the script has appropriate permissions to access the Unbound control socket.

For more examples and advanced usage, refer to the [Unbound docs](https://unbound.docs.nlnetlabs.nl/en/latest/getting-started/configuration.html#set-up-remote-control).

### Install

To get started, install the library using your preferred package manager:

#### Using npm:

```bash
npm install unbound-control-ts
```

#### Using yarn:

```bash
yarn add unbound-control-ts
```

### Example Usage

Here's a basic example to demonstrate how to use the library:

```ts
import { UnboundControl } from 'unbound-control-ts';

// Initialize the client with the path to the unbound-control binary
const unbound = new UnboundControl('/path/to/unbound-control');

// Fetch and display Unbound statistics
async function getStats() {
  try {
    const stats = await unbound.stats();
    console.log('Unbound Statistics:', stats);
  } catch (error) {
    console.error('Error fetching stats:', error);
  }
}

getStats();
```

## Development

### Develop Prerequisites

Before you begin, ensure you have the following tools installed on your system:

- **Node.js**: Version 16 or later. [Download Node.js](https://nodejs.org/)
- **npm**: Comes with Node.js, or install it separately if needed.
- **Unbound**: Ensure that `unbound-control` is installed and properly configured. Follow the [Unbound installation guide](https://nlnetlabs.nl/documentation/unbound/) for details.
- **TypeScript**: (Optional) For contributing to or extending the library, TypeScript must be installed globally or as a dev dependency.

### Develop Setup

Follow these steps to set up the project for local development:

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your-username/unbound-control-ts.git
   cd unbound-control-ts
   ```

2. **Install Dependencies**
   Use your preferred package manager to install dependencies:

   ```bash
   npm install
   ```

   or

   ```bash
   yarn install
   ```

3. **Build the Project**
   Compile the TypeScript source code into JavaScript:

   ```bash
   npm run build
   ```

4. **Run Tests**
   Verify the project by running tests:

   ```bash
   npm test
   ```

5. **Code Linting and Formatting**
   Use the following commands to ensure code quality:

   - Lint the code:

     ```bash
     npm run lint
     ```

   - Format the code:

     ```bash
     npm run format
     ```

## License

Distributed under the MIT License. See [LICENSE](./LICENSE) for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[issues-shield]: https://img.shields.io/github/issues/tsutsu3/unbound-control-ts?style=for-the-badge
[issues-url]: https://github.com/tsutsu3/unbound-control-ts/issues
[license-shield]: https://img.shields.io/github/license/tsutsu3/unbound-control-ts?style=for-the-badge
[license-url]: https://github.com/tsutsu3/unbound-control-ts/blob/master/LICENSE.txt
[npm-sheild]: https://img.shields.io/npm/dm/unbound-control-ts?style=for-the-badge&logo=npm

[npm-url]: https://www.npmjs.com/package/unbound-control-ts
[codecov-shield]: https://img.shields.io/codecov/c/github/tsutsu3/unbound-control-ts?token=KLIM50QN1V&style=for-the-badge&logo=codecov
[codecov-url]: https://codecov.io/gh/tsutsu3/unbound-control-ts
[codeclimate-shield]: https://img.shields.io/codeclimate/maintainability/tsutsu3/unbound-control-ts?style=for-the-badge&logo=codeclimate
[codeclimate-url]: https://codeclimate.com/github/tsutsu3/unbound-control-ts/maintainability