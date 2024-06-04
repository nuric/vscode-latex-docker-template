# vscode-latex-docker-template

A minimal VS Code LaTex template using Docker containers to compile. It contains the configuration to get VS Code up and running for LaTex with Docker. Some of the configured features include:

- GitHub Action to compile on push and have the PDF ready as an artifact.
- Install the essential extensions using `.vscode/extensions.json` for LaTex and spell checking.
- Adjust settings of LaTex to utilise a Docker container for compiling the project.
- Uses the same Docker container locally and for CI to ensure consistency.
- Format and compile on file save.
- Invert PDF colours using the extension settings, `.vscode/settings.json`.

The main motivation behind this setup is the extremely tedious and unhelpful native LaTex installation process. Using a Docker container to wrap `pdflatex` and more allows for a cleaner and more reproducible workspace.

## Getting started

Use the "Use this template" button to create a new repository with this template. Clone the repository and open it in VS Code. The first time you open the project, you will be prompted to install the recommended extensions. Click "Install All" to install them.

To compile the latex project:

1. Open the [main.tex](main.tex) file and find TEX extension in the left sidebar. It appears only when you have the LaTex Workshop extension installed and have a Tex file open.
2. Click the "Build LaTeX project" button to compile the project. The PDF will be generated using the Docker container.
3. After the compilation, click the "View LaTeX PDF" option button to view the generated PDF!

When you push, the same compilation process will be run on GitHub Actions. The PDF will be available as an artifact in the actions tab.

## Contributing

The objective is to keep this template as minimal as possible. For issues, suggestions, or improvements, please open an issue or a pull request.

## Built using

- [latex-docker](https://github.com/xu-cheng/latex-docker) is the Docker container that provides a full LaTex environment
- [latex-action](https://github.com/xu-cheng/latex-action) for the GitHub Action that compiles the project using the Docker container above
- [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) LaTex extension for VS Code
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) for checking all spelling in the project
