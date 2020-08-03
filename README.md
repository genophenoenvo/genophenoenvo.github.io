# calliope.github.io

Bootstrap.js and ReadTheDocs `github.io` website for GenoPhenoEnvo project

## Website development

To develop upon locally:
```
git clone https://github.com/genophenoenvo/genophenoenvo.github.io.git
cd genophenoenvo.github.io
npm install
npm run serve
```

**Important:** The ReadTheDocs are maintained in a separate GitHub Repo and are built using Sphinx. You must clone that repo separately, modify it, and then copy the contents of the `_build_html` into the `/docs` folder in this repository to update the ReadTheDocs

Managing the navbar Edit views/Navbar/pages.json to change the links at the top of the page.

Controllers, custom views Most pages should be able to just use `controllers/VanillaController.js`, that manages the navbar at the top and the footer at the bottom (`<header>` and `<footer>` tags are needed in the page's HTML for these to work).

The custom views in place (such as the header and footer) use the uki.js MVC framework; using the framework is optional, or feel free to include your own.

npm libraries Feel free to `npm install --save` any libraries that you need, but you will also need to edit .gitignore to specifically include the files that you actually link to inside node_modules (so that we don't end up committing the whole directory structure).
