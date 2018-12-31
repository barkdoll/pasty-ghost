# Pasty Ghost

A blank, dev-ready [Ghost](https://ghost.org/) theme inspired by Nahuel Sanchez's [Pale Ghost](https://github.com/nahuelsanchez/pale-ghost) theme.

Some npm tools have been added to make development easier by utilizing Sass (actually SCSS, 'cause who uses regular Sass these days).

## Getting Started

### Requirements
- [Ghost-supported version](https://docs.ghost.org/faq/node-versions/) of __Node.js__ (+__npm__)
- [local Ghost dev environment](https://docs.ghost.org/install/local/)
- some beginner Sass skills (actually SCSS)
- the motivation to read the simple steps below

### Setup

1. Clone this repo into your local ghost installation's theme folder
    ```
    cd /path/to/ghost/content/themes
    git clone https://github.com/barkdoll/pasty-ghost
    ```  

1. Navigate to this project's directory
    ```
    cd /path/to/repo/you/just/cloned
    ```

1. Install dev tools by running
    ```
    npm install
    ```

1. During development, you can run
    ```
    npm run dev
    ```
    to make npm watch your Sass files for changes and automatically compile them to CSS when changes are saved.

## Building your theme on top of Pasty Ghost

Now all that's left is building your theme, the fun part!

1. Make sure you are running the sass watcher npm script from step #4 in the [setup section](#setup) above.
    ```
    npm run dev
    ```

1. Open the theme directory in your IDE/text editor

1. Create a new __*.scss__ file in the theme assets directory:

    The theme assets directory: `/pasty-ghost/assets/sass`
    
    Example: `my-theme.scss`

1. Add a link to a file with the same name and a `.css` extension instead of `.scss` it in the theme's head template file. You should add it after the last listed stylesheet link so that your styles are applied on top of the base styles. 

    The head template file: `/pasty-ghost/partials/core/head.hbs`

    ```html
    <link href="{{asset "css/mytheme.css"}}" rel="stylesheet" type="text/css" />
    ```

1. Add your styles and build your theme. Good luck!

## Credits

Sass watcher npm scripts implemented courtesy of [@hellobrian](https://github.com/hellobrian)'s [node-sass recipe](https://github.com/hellobrian/sass-recipes/tree/master/node-sass#using-node-sass).