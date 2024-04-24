**zipapp-llm**

This script creates a ZIP application from a Python package called `llm` and exports it as `llm.pyz`.

To use this script, follow these steps:

1. Clone this repository to your local machine using `git clone <repository-url>`
2. Navigate into the cloned repository and run the `build` script by executing `./build`

The script will create a new virtual environment using Python 3, install the required packages, including `pydantic` version less than 2 and the `llm-ollama` plugin, and then create a ZIP application from the installed package. The resulting ZIP application will be saved as `llm.pyz`.

**Prerequisites**

* Python 3 must be installed on your system
* Git must be installed on your system to clone this repository

**Notes**

* This script is designed for use on Linux systems. If you are using a Windows or macOS system, you may need to modify the script to accommodate differences in file paths and package installation.
* The `SKIP_CYTHON` environment variable is set to 1 in this script, which means that Cython compilation will be skipped. Pydantic 2 depends on cython and dynamic modules cannot be used in zipapps.
