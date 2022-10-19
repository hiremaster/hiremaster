# Develop Setup

## Run the code

- First create and activate your virtualenv - with the `venv` package on OSX or Linux, this will be:

```bash
python3 -m venv my_venv
source my_venv/bin/activate
```

- Clone the source codes from Github to local machine

```
git clone https://github.com/Wright-Media/hiremasterai-backend
```

- With your virtualenv active, install the project locally:

```bash
pip install -r requirements.txt
```

- And now you should be able to run the service like this:

```bash
make
```

## Installation tensorflow on M1-Chip Mac

```python
# Not required currently
```

```
conda install -c apple tensorflow-deps -y
python -m pip install tensorflow-macos
pip install tensorflow-metal
```

```
conda install -c conda-forge jupyter jupyterlab -y
jupyter lab
```
