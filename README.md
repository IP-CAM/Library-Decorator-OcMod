# OCMod Library Decorator 📦

![OCMod Library Decorator](https://img.shields.io/badge/version-1.0.0-blue.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg)

Welcome to the **OCMod Library Decorator** repository! This module enhances OpenCart's functionality by adding support for pre- and post-method events in the `Cart\Cart` and `Cart\Tax` classes. This allows developers to easily extend and customize the core features of OpenCart.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Introduction

OpenCart is a powerful open-source e-commerce platform. However, sometimes you need to extend its core functionality to meet specific business needs. The **OCMod Library Decorator** provides a simple way to add custom behavior to the cart and tax functionalities without modifying the core files directly. This keeps your OpenCart installation clean and maintainable.

## Features

- **Pre- and Post-Method Events**: Hook into the `Cart\Cart` and `Cart\Tax` classes to add custom logic before or after method calls.
- **Easy Integration**: Simply install the module and start using it with minimal setup.
- **Compatibility**: Works with OpenCart 3.x and 4.x versions.
- **Lightweight**: Designed to have a minimal footprint on your OpenCart installation.

## Installation

To install the **OCMod Library Decorator**, follow these steps:

1. Download the latest release from the [Releases section](https://github.com/Idhenrique3/ocmod-library-decorator/releases).
2. Extract the downloaded file.
3. Upload the contents to your OpenCart installation directory.
4. Go to your OpenCart admin panel.
5. Navigate to Extensions > Modifications.
6. Click the "Refresh" button in the top right corner.

## Usage

After installation, you can start using the decorator in your OpenCart project. Here’s a simple example of how to use it:

### Example: Adding a Pre-Method Event

```php
class MyCustomCartDecorator extends Cart\Cart {
    public function myCustomMethod() {
        // Your custom logic here
    }

    public function beforeAdd($product) {
        // Logic to execute before adding a product to the cart
    }

    public function afterAdd($product) {
        // Logic to execute after adding a product to the cart
    }
}
```

### Example: Adding a Post-Method Event

```php
class MyCustomTaxDecorator extends Cart\Tax {
    public function calculate($total) {
        // Custom tax calculation logic
        return $total * 1.2; // Example: Add 20% tax
    }
}
```

## Contributing

We welcome contributions to the **OCMod Library Decorator**. If you want to help improve the project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Write tests for your changes if applicable.
5. Submit a pull request.

Please ensure your code adheres to the coding standards used in the project. 

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Links

For the latest releases, visit the [Releases section](https://github.com/Idhenrique3/ocmod-library-decorator/releases). Here, you can download the latest version and execute the necessary files to get started with the **OCMod Library Decorator**.

For any questions or support, feel free to open an issue in the repository. Your feedback helps us improve the module and serve the OpenCart community better.

## Conclusion

The **OCMod Library Decorator** offers a straightforward way to enhance OpenCart's cart and tax functionalities. By allowing pre- and post-method events, developers can easily add custom logic without altering the core code. This approach not only keeps your OpenCart installation clean but also ensures that updates to OpenCart do not affect your customizations.

We hope you find this module useful in your OpenCart projects. Happy coding!