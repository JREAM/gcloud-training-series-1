# Google Cloud SDK

This is a CLI (Command Line) Application. You can visit 
[https://cloud.google.com/sdk/install](https://cloud.google.com/sdk/install) there.


- **Requires** Python 2.7.x 
  - OSX and Ubuntu should already have it.
  - In windows download at [Python 2.7.15](https://www.python.org/downloads/release/python-2715/)
    - Go with **Windows x86-64 MSI installer**
    - When Installing, make sure that "Include in PATH" is checked

Ensure you have python:

```sh
python -V
```

## For Mac OSX

Download from here [Quickstart for macOS](https://cloud.google.com/sdk/docs/quickstart-macos)

## For Windows

Download from here [Quickstart for Windows](https://cloud.google.com/sdk/docs/quickstart-windows)

## For Ubuntu/Mint

Run the following (We manually place bionic incase you are on Mint 19):

```sh
export CLOUD_SDK_REPO="cloud-sdk-bionic"
echo "deb http://packages.cloud.google.com/apt $CLOUD_SDK_REPO main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
sudo apt-get update && sudo apt-get install google-cloud-sdk
```

## Initialize the SDK

I suggest doing this after we go through the GCP Console (UI), we must
create a project.

For every OS.

```sh
gcloud init
```

Follow the steps and login.

