<!-- [![Build Status](https://travis-ci.org/cyber-fighters/SemantiX.svg?branch=master)](https://travis-ci.org/cyber-fighters/SemantiX) -->

# KeyworX

## Goal
Keyword-based document search

# Execution
The pipeline consists of the following steps:
* `data_mining`: gather the text data and save to pickle file
* `data_exploration`: display and explore the data

## Setup

### Files
The file `data/paths.json` collects hardcoded paths to data files or other descriptive names of data attributes and has to be created by the user himself. It is not included in the repo for privacy reasons. Example contents:
```json
{
  "keywords": {
    "file": "data/my_file_with_confidential_name.docx"
  },
  "data": {
    "directory": ["data/confidential_data_0", "data/confidential_data_0"],
    "test": "test_email_file.msg"
  }
}

```

### Installation
* download [python](https://www.python.org/downloads/) (>= 3.6) for windows (includes `pip`)
* install [pipenv](https://pipenv.readthedocs.io): `pip install pipenv`
* install everything using `pipenv install`
* start shell of virtual environment (VE): `pipenv shell`
* force Jupyter to use correct kernel
	* install kernel of correct VE with `python -m ipykernel install --user`
	* verify with
		```python
		import sys
		sys.executable
		```
* have fun!
	
### Install git hooks
To keep commits in a good style, some checks are executed at different stages of the git work stream. Run
```shell
./.githook/install-hooks.sh
```
to install the hooks.
