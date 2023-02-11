# Deep RL Bootcamp

## Setup (once)

Install Conda.
- https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html

Install Docker Desktop.
- https://www.docker.com/products/docker-desktop/
- Start Docker to symlink binaries into `bin` folder.

Install XQuarts (aka X.Org for MacOS)
```shell
brew install --cask xquartz
defaults write org.xquartz.X11 nolisten_tcp -bool false
defaults write org.xquartz.X11 enable_iglx -bool true
```

Create environment
```sh
conda env create -f environment.yml
```

Download premade Docker image:
```shell
 docker pull dementrock/deeprlbootcamp:latest
```

## Setup (every time)
Activate Conda environment.
```sh
conda activate deeprlbootcamp
```

Make sure Docker daemon is running.

Start Jupyter Notebook.
```shell
jupyter notebook
```

## Procedures

### Update environment with modified environment.yml
Remove packages not in `environment.yml`.
Add packages from `environment.yml`.
```sh
conda activate deeprlbootcamp
conda env update -f environment.yml --prune
```