# Node Documentation

## Build
This doc is built on *mdBook*. To quote them directly:

"mdBook is a command line tool to create books with Markdown"

All things about the operation of mdBook can be found in its documentation: https://rust-lang.github.io/mdBook/

Even so here are some important parts:

1. The `book` file is the built book of HTML built from relevant .md's. DO NOT make any meaningful changes here as these files will just be replaced. When the book is re-built.
2. The `src` file contains all the source .md's that all the pages of the docs are built from. If you are to make a change, do it in here.
3. The `theme` file contains all the information about how the book looks. There are many default themes, but the ones used by this book are "light" and "navy".
 - You can change a variety of the colors of a book theme via the `custom.css` file.
4. The `book.toml` file contains some key functionality and rendering settings of the book. Have a look at the "Configuring Renderers" section of the mdBook documentation linked above.


To run/build/locally host the mdBook, one first has to install the mdBook CLI tool and a couple dependencies (follow directions here: https://rust-lang.github.io/mdBook/guide/installation.html).

To then actually build the book and locally host it: 

- In the `CreatorNodeDocumentation` directory
- run `mdbook serve`
- Go to http://localhost:3000

For more info see: https://rust-lang.github.io/mdBook/cli/serve.html

## Deploy
XXX