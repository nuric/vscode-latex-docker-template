# vscode-latex-docker-template

A minimal VS Code LaTex template using Docker containers to compile. It contains the configuration to get VS Code up and running for LaTex with Docker. Some of the configured features include:

- GitHub Action to compile on push and have the PDF ready as an artifact.
- Install the essential extensions using `.vscode/extensions.json` for LaTex and spell checking.
- Adjust settings of LaTex to utilise a Docker container for compiling the project.
- Uses the same Docker container locally and for CI to ensure consistency.
- Format and compile on file save.
- Invert PDF colours using the extension settings, `.vscode/settings.json`.

The main motivation behind this setup is the extremely tedius and unhelpful native LaTex installation process. Using a Docker container to wrap `pdflatex` and more allows for a cleaner and more reproducible workspace.

## Built using

- [latex-docker](https://github.com/xu-cheng/latex-docker) is the Docker container that provides a full LaTex environment
- [latex-action](https://github.com/xu-cheng/latex-action) for the GitHub Action that compiles the project using the Docker container above
- [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) LaTex extension for VS Code
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) for checking all spelling in the project
