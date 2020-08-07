# genophenoenvo.github.io

Bootstrap.js and ReadTheDocs `github.io` website for GenoPhenoEnvo project

## Website development

To develop upon locally:
```
git clone https://github.com/genophenoenvo/genophenoenvo.github.io.git
cd genophenoenvo.github.io
npm install
npm run serve
```

**Important:** The ReadTheDocs are maintained in a separate GitHub Repo and are built using Sphinx. You must clone that repo separately, modify it, and then copy the contents of the `./readthedocs/` sub-directory into the `/readthedocs` folder in this repository to update the ReadTheDocs

Managing the navbar Edit views/Navbar/pages.json to change the links at the top of the page.

Controllers, custom views Most pages should be able to just use `controllers/VanillaController.js`, that manages the navbar at the top and the footer at the bottom (`<header>` and `<footer>` tags are needed in the page's HTML for these to work).

The custom views in place (such as the header and footer) use the uki.js MVC framework; using the framework is optional, or feel free to include your own.

npm libraries Feel free to `npm install --save` any libraries that you need, but you will also need to edit .gitignore to specifically include the files that you actually link to inside node_modules (so that we don't end up committing the whole directory structure).

### ReadTheDocs (RTD) Documentation sub-section

The repo supports a the [Read the Docs documentation](https://readthedocs.org/) documentation in use by the GenoPhenoEnvo project. 

#### Goals of the RTD

The goal of the documentation should beto provide basic learning materials to help researchers, educators, and students effectively (re)use our research material in the CyVerse cyberinfrastructure. 

All documentation is considered a work-in-progress; even the best efforts will be incomplete, contain ambiguities, inaccuracies, and at some point, will become out of date. 

#### Maintained Sections

We maintain the following templates. All documentation in the should be derived from these. They can be adapted slightly, but documentation should strive to be consistently formatted. 

    - URL: https://github.com/genophenoenvo/readthedocs
    
- **Research**: Specific explanations of the research and how to reproduce it

- **Data Sources**: Information about the data sets we're using in the project

- **Documentation**: Explanation of where data sets are located and how to (re)create our workflows.

- **Tutorials**: Tutorials to teach how to use our platforms. 

- **Publications:**: Presentations and peer-reviewed work conducted on the award.

#### Making Changes to the RTD portion of our website

This repository contains all of the necessary build material to generate a ReadTheDocs website

Because we're using a separate Bootstrap.js website for our main page, this repository is necessary for rendering the `html` components of the documentation.

To build the ReadTheDocs pages, you must install [Sphinx](https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html) on your local computer

After you've installed Sphinx, you should be ready to edit the documentation pages:

```
git clone https://github.com/genophenoenvo/genophenoenvo.github.io/
genophenoenvo.github.io/
sphinx-autobuild -b html --host 0.0.0.0 --port 8000 --poll . readthedocs
```
