## Comparison of main logos

Steps to convert a set of `*.svg` into `.png`:

- Copy all target `*.svg` files into this directory.

- Apply the following commands from this directory (requires `imagemagick`):

    - 'mini.nvim' logo (`nvim_*.svg`):

        ```sh
        magick mogrify -format png -density 300 -resize x105 nvim_*.svg
        ```

    - MiniMax logo (`minimax_*.svg`):

        ```sh
        magick mogrify -format png -density 300 -resize x105 minimax_*.svg
        ```

    - MINI logo (`mini_*.svg`):

        ```sh
        magick mogrify -format png -density 300 -resize x1000 mini_*.svg
        ```

    - MINI circled logo (`mini-circle_*.svg`):

        ```sh
        magick mogrify -format png -density 300 -resize x1000 mini-circle_*.svg
        ```
