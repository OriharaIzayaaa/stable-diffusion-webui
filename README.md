# Stable Diffusion web UI
A browser interface based on Gradio library for Stable Diffusion.

This fork including the full package of UI and models.

![](screenshot.png)

## Installation and Running
Make sure the required [dependencies](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Dependencies) are met and follow the instructions available for both [NVidia](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and-Run-on-NVidia-GPUs) (recommended) and [AMD](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Install-and-Run-on-AMD-GPUs) GPUs. Alternatively, use online services (like Google Colab).

### Installation on an online service

- [GoogleColab](https://githubtocolab.com/OriharaIzayaaa/stable_diffusion_colab/blob/main/GoogleColab_stable_diffusion.ipynb) (Note that this requires a Colab Pro subscription)
- [Runpod](https://blog.runpod.io/stable-diffusion-ui-on-runpod/)
- [Paperspaces](https://blog.paperspace.com/stable-diffusion-webui-deployment/)


### Automatic Installation on Windows
1. Install [Python 3.10.6](https://www.python.org/downloads/release/python-3106/) (Newer version of Python does not support torch), checking "Add Python to PATH".
2. Install [git](https://git-scm.com/download/win).
3. Download the stable-diffusion-webui repository, for by running `git clone https://github.com/OriharaIzayaaa/stable-diffusion-webui.git`.
4. Run `webui-user.bat` from Windows Explorer as normal, non-administrator, user. (The installation might take some while)

### Automatic Installation on Linux
1. Install the dependencies:
```bash
# Debian-based:
sudo apt install wget git python3 python3-venv
# Red Hat-based:
sudo dnf install wget git python3
# Arch-based:
sudo pacman -S wget git python3
```
2. Navigate to the directory you would like the webui to be installed and execute the following command:
```bash
bash <(wget -qO- https://raw.githubusercontent.com/OriharaIzayaaa/stable-diffusion-webui/master/webui.sh)
```
3. Run `webui.sh`.
4. Check `webui-user.sh` for options.

### Installation on Apple Silicon
1. If Homebrew is not installed, follow the instructions at https://brew.sh to install it. Keep the terminal window open and follow the instructions under "Next steps" to add Homebrew to your PATH.
2. Open a new terminal window and run `brew install cmake protobuf rust python@3.10 git wget`
3. Clone the web UI repository by running `git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui`
4. Place Stable Diffusion models/checkpoints you want to use into `stable-diffusion-webui/models/Stable-diffusion`. If you don't have any, see Downloading Stable Diffusion Models below.
5. `cd stable-diffusion-webui` and then `./webui.sh` to run the web UI. A Python virtual environment will be created and activated using venv and any remaining missing dependencies will be automatically downloaded and installed.
To relaunch the web UI process later, run `./webui.sh` again.

## Models

While there are a lot of models (check out e.g. [huggingface](https://huggingface.co/)) the following point gives a good starting point. 
Note that SDXL based models have stronger requirements regarding hardware.

There are two supported file formats `.ckpt` and `.safetensor`. It is higly recommended to only use `.safetensor` files as other formates can contain malicious code.

- [Stable Diffusion 1.5](https://huggingface.co/stable-diffusion-v1-5) ([v1-5-pruned-emaonly.safetensor](https://huggingface.co/stable-diffusion-v1-5/stable-diffusion-v1-5/blob/main/v1-5-pruned-emaonly.safetensors))
- [Stable Diffusion XL 1.0](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0) ([sd_xl_base_1.0.safetensor](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0/blob/main/sd_xl_base_1.0.safetensors))
- [General_XL_v8](https://drive.google.com/file/d/163HQ49s40ZG11FEtCs7CyVTMvYFHwjvV/view?usp=drive_link) (A general purpose finetuned model based on SDXL)

## Documentation
A full documentation for the UI is at the [wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki) (note that it might refer to a different, unstable version).

## Notes

- All images are automatically saved in the `Output` folder

