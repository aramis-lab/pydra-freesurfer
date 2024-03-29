# pydra-freesurfer

[![PyPI - Version][pypi-version]][pypi-project]
[![PyPI - Python Version][pypi-pyversions]][pypi-project]
[![PyPI - Downloads][pypi-downloads]][pypi-project]
![][status-docs]
![][status-test]

----

Pydra tasks for FreeSurfer.

[Pydra][pydra] is a dataflow engine
which provides a set of lightweight abstractions
for DAG construction, manipulation, and distributed execution.

[FreeSurfer][freesurfer] is a neuroimaging toolkit
for processing, analyzing, and visualizing human brain MR images.

This project exposes some of FreeSurfer's utilities as Pydra tasks
to facilitate their integration into more advanced processing workflows.

**Table of contents**

- [Available interfaces](#available-interfaces)
- [Installation](#installation)
- [Development](#development)
- [Licensing](#licensing)

## Available interfaces

| Module    | Interfaces                                                                                          |
|-----------|-----------------------------------------------------------------------------------------------------|
| gtmseg    | GTMSeg                                                                                              |
| mri       | Aparc2Aseg, Binarize, Convert, Coreg, Label2Vol, RobustRegister, RobustTemplate, Surf2Surf, Vol2Vol |
| mris      | AnatomicalStats, CALabel, CATrain, Expand, Preproc                                                  |
| recon_all | ReconAll, BaseReconAll, LongReconAll                                                                |

## Installation

```console
pip install pydra-freesurfer
```

A separate installation of FreeSurfer is required to use this package.
Please review the following [instructions][freesurfer-install]
and [licensing details][freesurfer-license].

## Development

This project is managed with [Hatch][hatch]:

```console
pipx install hatch
```

To run the test suite:

```console
hatch run test
```

To fix linting issues:

```console
hatch run lint:fix
```

To check the documentation:

```console
hatch run docs:serve --open-browser
```

## Licensing

This project is distributed under the terms of the [Apache License, Version 2.0][license].

[freesurfer]: https://surfer.nmr.mgh.harvard.edu

[freesurfer-install]: https://surfer.nmr.mgh.harvard.edu/fswiki/DownloadAndInstall

[freesurfer-license]: https://surfer.nmr.mgh.harvard.edu/registration.html

[hatch]: https://hatch.pypa.io

[license]: https://opensource.org/licenses/Apache-2.0

[pydra]: https://nipype.github.io/pydra

[pypi-downloads]: https://static.pepy.tech/badge/pydra-freesurfer

[pypi-project]: https://pypi.org/project/pydra-freesurfer

[pypi-pyversions]: https://img.shields.io/pypi/pyversions/pydra-freesurfer.svg

[pypi-version]: https://img.shields.io/pypi/v/pydra-freesurfer.svg

[status-docs]: https://github.com/aramis-lab/pydra-freesurfer/actions/workflows/docs.yaml/badge.svg

[status-test]: https://github.com/aramis-lab/pydra-freesurfer/actions/workflows/test.yaml/badge.svg
