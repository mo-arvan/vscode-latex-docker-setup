# Latex Docker Setup in VS Code

## Features

- Dockerfile is based on ``mirisbowring/texlive_ctan_full:2019`` which comes with the support for texlive 2019
- latexindent is fully supported
- seamless git integration

## Prerequisites
- Docker
- git
- ssh
- VS Code

## Instructions

Clone this repository using the command below:

```bash
ssh clone git@github.com:mo-arvan/latex-docker-setup.git
```

Create directory named ``workspace`` inside repository's root directory.

``
cd {PATH_TO_REPO}/latex-docker-setup
mkdir workspace
``

Open VS Code and the [Remote - Container](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension.

Inside the VS Code, press ``F1``, type in ``Remote-Containers`` and then select ``Open Workspace In Container...`` from the dropdown menu. In the pop-out window, select ``latex-docker-setup/settings.workspace``. Wait until the docker image is downloaded and built. 

Once the VS Code is fully loaded, you need to add your projects to the active workspace. In order to do so, you must add/copy your tex projects in the workspace directory. I recommend creating a git repository for each project and cloning them in the workspace. 

``
mkdir workspace/tex-example-project
touch workspace/tex-example-project/example.tex

OR 

cd workspace
git clone {PROJECT_REPO}
``
Lastly, insert the path of the project to the ``settings.code-workspace``. 

``
{
	"folders": [
    {
      "path": "workspace/example"
    },
    {
      "path": "."
    }
  ],
	"settings": {
		"editor.tabSize": 2, 
		"editor.insertSpaces": true,
		"editor.detectIndentation": false,
		"editor.wordWrap": "on",
		"latex-workshop.latex.outDir": "%DIR%/out",
		"latex-workshop.synctex.afterBuild.enabled": true
	}
}
``

That's it. All you need to do now is to open a ``.tex`` file, you can use ``ctrl + shift + B`` to compile and ``ctrl + shift + V`` to view the compiled file. 

## Credits

- vs-code docker setup: https://medium.com/@kombustor/vs-code-docker-latex-setup-f84128c6f790
- ssh keys: https://github.com/docker-library/golang/issues/148#issuecomment-355082955
