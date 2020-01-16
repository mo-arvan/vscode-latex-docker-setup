# Latex Docker Setup in VS Code

## Features

- texlive 2019 (latest)
- latexindent is fully supported
- seamless git integration

## Instructions

Clone this repository using the command below:

```bash
ssh clone git@github.com:mo-arvan/latex-docker-setup.git
```

Create a ``workspace`` directory inside ``latex-docker-setup`` and add/copy your projects to that dir.
Install VS Code and the [Remote - Container](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension.

Inside the VS Code, press ``F1``, type in ``Remote-Containers`` and then select ``Open Workspace In Container...`` from the dropdown menu.

Once the VS Code is fully loaded, you can add your projects to the active workspace.

## Credits

Overall setup: https://medium.com/@kombustor/vs-code-docker-latex-setup-f84128c6f790
ssh keys: https://github.com/docker-library/golang/issues/148#issuecomment-355082955
