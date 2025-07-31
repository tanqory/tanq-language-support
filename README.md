# Tanq Language Support for VS Code

[](https://www.google.com/search?q=https://marketplace.visualstudio.com/items%3FitemName%3Dtanqory.tanq-language-support)
[](https://www.google.com/search?q=https://marketplace.visualstudio.com/items%3FitemName%3Dtanqory.tanq-language-support)

-----

## Overview

The **Tanq Language Support** extension brings enhanced development experience for `.tanq` files right into Visual Studio Code. If you're working with Tanq, this extension provides crucial features like **syntax highlighting** for both the Nunjucks-like template part and the embedded JSON model block, along with a **distinct file icon**.

-----

## Features

  * **Syntax Highlighting:** Get proper syntax highlighting for:
      * **Nunjucks-like Templates:** The HTML structure with `{{ ... }}` expressions and `{% ... %}` blocks will be colored correctly, similar to Jinja2 or Liquid templates.
      * **Embedded JSON Block:** The `{% block model %} ... {% endblock %}` section, which contains your JSON model definition, will receive dedicated JSON syntax highlighting, making it easy to read and validate.
  * **Tanq File Icon:** Files with the `.tanq` extension will display a unique icon in the VS Code Explorer, helping you quickly identify your Tanq files.

-----

## Installation

You can install the **Tanq Language Support** extension directly from the Visual Studio Code Marketplace:

1.  Open VS Code.
2.  Go to the Extensions view (`Ctrl+Shift+X` or `Cmd+Shift+X`).
3.  Search for "Tanq Language Support".
4.  Click **Install**.

Alternatively, you can install it via the VS Code Marketplace website: [https://marketplace.visualstudio.com/items?itemName=tanqory.tanq-language-support](https://www.google.com/search?q=https://marketplace.visualstudio.com/items%3FitemName%3Dtanqory.tanq-language-support)

-----

## Usage

Simply open any file with a `.tanq` extension in VS Code. The extension will automatically apply the syntax highlighting and display the custom file icon.

**Example `*.tanq` file structure:**

```tanq
<div>
    <h1>{{ block.props.title }}</h1>
    <p>This is the Nunjucks-like template part, rendering dynamic content.</p>
    {% if block.props.showImage %}
        <img src="{{ block.props.imageUrl }}" alt="{{ block.props.imageAlt }}">
    {% endif %}
</div>

{% block model %}
{
    "type": "block",
    "title": "block-name",
    "icon": "icon-name",
    "zones": [
        {
            "name": "default",
            "displayName": "Default Zone"
        }
    ],
    "fields": {
        "title": {
          "type": "text",
          "title": "Block Title"
        },
        "showImage": {
          "type": "boolean",
          "title": "Show Image",
          "default": false
        },
        "imageUrl": {
          "type": "text",
          "title": "Image URL"
        },
        "imageAlt": {
          "type": "text",
          "title": "Image Alt Text"
        }
    },
    "components": [],
    "defaultComponents": []
}
{% endblock %}
```

-----

## Contributing

If you encounter any issues or have suggestions for improvements, feel free to open an issue or submit a pull request on the [GitHub repository](https://www.google.com/url?sa=E&source=gmail&q=https://github.com/tanqory/tanq-language-support).

-----

## License

This extension is licensed under the [MIT License](LICENSE.md).

-----

## Release Notes

### 0.0.1

Initial release of Tanq Language Support.

  - Adds syntax highlighting for `.tanq` files (Nunjucks-like HTML + embedded JSON).
  - Provides a custom file icon for `.tanq` files.