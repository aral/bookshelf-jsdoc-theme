# How to contribute to Bookshelf theme

Start by installing dependencies:

    npm install

Link your local copy of the theme with Bookshelf:

    npm link # in bookshelf-jsdoc-theme's directory
    npm link bookshelf-jsdoc-theme # in bookshelf's directory

Everything is ready to start building the docs with your local copy of the theme. In your bookshelf directory just run:

    npm run jsdoc

If you edit any of the `.scss` files you need to build the static stylesheet first:

    npm run build

### Publishing on npm

Ensure you have publish rights for the package. Then just follow these steps:

    # Increment the version using one of "major", "minor", or "patch" according to the scope of
    # changes introduced, and also provide a commit message (optional):
    npm version major -m "Update version number"

    # Push changes to remote
    git push
    git push --tags

    # Publish on npm
    npm publish
