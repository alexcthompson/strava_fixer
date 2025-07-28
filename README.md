# Strava GPS fixer

At the current time, this is not a user friendly tool, unless you are familiar with Strava, including the ins and outs of downloading and uploading GPX files for activities, and familiar with Jupyter notebooks.

I was doing a lot of trail runs in deep forest in 2017/2018, and tracking my runs using a phone GPS.  At some point I got sick of having terrible GPS tracks which gave exaggerated and erratic speed, distance and elevation readings.  So I hacked together a tool to smooth out jumpy GPS tracks.

## Install

Install the environment with `mamba` using `conda-forge` plus the following dependencies:

```
jupyterlab
black
jupyter-black
pre_commit
pytest
ipytest
numpy
scikit-learn
plotly
```

`gpxpy` is a Python library for parsing GPX files, the file format for Strava activities.  Install it with:

```
pip install gpxpy
```

## Contributing

Black Python formatter is used in this project with the setting `--line-length=100`. It is recommended that you add a pre-commit hook to enforce this using [Black's version control integration documentation](https://black.readthedocs.io/en/stable/integrations/source_version_control.html). A version of `.pre-commit-config.yaml` is included in this project's root directory, including the necessary arg for line length, and will be installed with:

```
$ pre-commit install
```

[`nbstripout`](https://github.com/kynan/nbstripout) is used to remove output from Jupyter Notebooks.  Install `nbstripout` with:

```
pip install --upgrade nbstripout
```

and add a git filter with:

```
nbstripout --install
```
