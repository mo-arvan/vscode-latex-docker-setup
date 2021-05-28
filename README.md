# Latex Docker Setup in VS Code

## Features

- Dockerfile is based on ``mirisbowring/texlive_ctan_full:2019`` which comes with the support for texlive 2019
- latexindent is fully supported
- seamless git integration

## Instructions

Clone this repository using the command below:

```bash
ssh clone git@github.com:mo-arvan/latex-docker-setup.git
```

Create directory named ``workspace`` inside repository's root directory and add/copy your tex projects there.
Install VS Code and the [Remote - Container](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension.

Inside the VS Code, press ``F1``, type in ``Remote-Containers`` and then select ``Open Workspace In Container...`` from the dropdown menu.

Once the VS Code is fully loaded, you can add your projects to the active workspace. Once you open a ``.tex`` file, you can use ``ctrl + shift + B`` to compile and ``ctrl + shift + V`` to view the compiled file. 

## Credits

Overall setup: https://medium.com/@kombustor/vs-code-docker-latex-setup-f84128c6f790
ssh keys: https://github.com/docker-library/golang/issues/148#issuecomment-355082955
