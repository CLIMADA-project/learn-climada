# The CLIMADA Teaching Materials Collection

This project collects all materials for learning climate risk assessment with CLIMADA and compiles them into an (interactive) [Jupyter Book](https://jupyterbook.org/).

## Build Instructions

To build the book locally, follow these instructions (assuming you have Mamba installed):

1. Install Jupyter Book into a suitable environment:

   ```
   mamba install -n <my-env> "jupyter-book"
   ```

2. Enter the environment:

   ```
   mamba activate <my-env>
   ```

3. Set up a local server hosting the book:

   ```
   jupyter book start
   ```

The URL to the server will be displayed. By default, it's `http://localhost:3000`.
You can access the book via this URL with your browser.
