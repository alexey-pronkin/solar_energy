## Install environment

- Install miniconda https://docs.conda.io/en/main/miniconda.html

### MacOS

```bash
conda env create -f environment_macos.yml
```

### Linux
- Create env:
```bash
conda create --name solar --file requirements.txt
```

If you using macos or windows, alternative install:

```bash
conda create --name solar python=3.10.9 -y
conda run -n solar python -m pip install -r requirements_docker.txt -y
```

- activate env
```bash
conda activate solar
```
## Run code

Run jupyter notebook 
```sh
jupyter notebook
```

## Docker

```bash
sudo docker build . -t solar:latest
sudo sudo docker run --gpus all --interactive --tty -v ${pwd}/docker_folder:/home/user/docker/ docker-tcvc:latest
```