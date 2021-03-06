# InvenTree Documentation

This repository hosts the [official documentation](https://inventree.readthedocs.io/) for [InvenTree](https://github.com/inventree/inventree), an open source inventory management system. 

To serve this documentation locally (e.g. for development), you will need to have Python 3 installed on your system.

## Setup

Run the following commands from the top-level project directory:

```
$ git clone https://github.com/inventree/inventree-docs
$ cd inventree-docs
$ python3 -m venv env-inv-doc
$ source env-inv-doc/bin/activate
$ pip install -r requirements.txt
```

## Serve Locally

To serve the pages locally, run the following command (from the top-level project directory):

```
$ mkdocs serve
``` 

## Edit Documentation Files

Once the server is running, it will monitor the documentation files for any changes, and update the served pages.

### Admonitions

"Admonition" blocks can be added as follow:
```
!!! info "This is the admonition block title"
    This is the admonition block content
```

Refer to the [reference documentation](https://squidfunk.github.io/mkdocs-material/reference/admonitions/) to customize the admonition block to the use-case (eg. warning, missing, info, etc.).

### Images

Images are served from the `./docs/assets/images` folder and can be added as follow:
```
{% with id="image_id", url="folder/image_name.png", description="Text shown if image is not loaded properly" %}
{% include 'img.html' %}
{% endwith %}
```

Replace:
* `image_id` with a short unique indentifier for the image (most commonly, `image_id` is same as `image_name`)
* `folder` with the folder in `docs/assets/images` in which the image is stored
* `image_name` with the name of the image
* `.png` with the image extension (PNG or JPEG are preferred formats)

### Global variables

Refer to the [reference documentation](https://squidfunk.github.io/mkdocs-material/reference/variables/#using-custom-variables) to find out how to add global variables to the documentation site.

Global variables should be added in the `# Global Variables` section of the `mkdocs.yml` configuration file.

## Credits

This documentation makes use of the [mkdocs-material template](https://github.com/squidfunk/mkdocs-material)
