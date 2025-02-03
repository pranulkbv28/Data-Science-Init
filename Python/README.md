# Introduction to Python for Data Science

## Prerequisites

- [Python](https://www.python.org/)
- **pip**: this comes bundled with `Python`.
- as for the place to practice `Python`, we will be using [Jupyter Lab](https://jupyter.org/install)

## Installation

1. After installing `Python` and `pip`, verify if you have the same

    - for `windows`

        ```bash
        python --version
        ```

    - for `mac`

        ```bash
        python3 --version
        ```

2. Let us now **install** `Jupyter Lab`

    - We are using `Jupyter Lab` because it is
        - more organized
        - feature-rich
        - extensible
    - While installing `Jupyter Lab`, we will be doing so in a `virtual environment` of `Python`
        - create the `virtual environment`

            - for `windows`

                ```powershell
                python -m venv jupyter-env
                ```

            - for `mac`

                ```bash
                python3 -m venv jupyter-env
                ```

        - activate the `virtual environment`

            - for `windows`

                ```powershell
                .\jupyter-env\Scripts\activate
                ```

            - for `mac`

                ```bash
                source jupyter-env/bin/activate
                ```

        - install `Jupyter Lab` inside the `virtual environment`

            ```bash
            pip install jupyterlab
            ```

        - run `Jupyter Lab`

            ```bash
            jupyter lab
            ```

3. Once `Jupyter Lab` runs, it opens in your default browser at [this link](http://localhost:8888/lab).
