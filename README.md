# singularity-nbia-data-retriever

A [Singularity](https://sylabs.io/singularity/) container for the [NBIA Data Retriever](https://wiki.cancerimagingarchive.net/display/NBIA/Downloading+TCIA+Images), a tool for downloading medical imaging data from [The Cancer Imaging Archive (TCIA)](https://www.cancerimagingarchive.net/).

## Versions

| Version | Base OS |
|---------|---------|
| 4.4.3 | Ubuntu 22.04 |

## Requirements

- [Singularity](https://sylabs.io/singularity/) (or [Apptainer](https://apptainer.org/))
- `sudo` privileges to build the image

## Building

```bash
cd 4.4.3
./build.sh
```

This runs:

```bash
sudo singularity build singularity-nbia-data-retriever.sif Singularity
```

## Usage

Run the container with a TCIA manifest file (`.tcia`):

```bash
singularity run singularity-nbia-data-retriever.sif [options]
```

Or execute the NBIA Data Retriever directly:

```bash
singularity exec singularity-nbia-data-retriever.sif /opt/nbia-data-retriever/bin/nbia-data-retriever [options]
```

## Notes

- The container is built on Ubuntu 22.04 with all required dependencies for the NBIA Data Retriever GUI.
- NBIA Data Retriever version 4.4.3 is installed from the [CBIIT/NBIA-TCIA GitHub releases](https://github.com/CBIIT/NBIA-TCIA/releases).

## References

- [NBIA Data Retriever Documentation](https://wiki.cancerimagingarchive.net/display/NBIA/Downloading+TCIA+Images)
- [The Cancer Imaging Archive (TCIA)](https://www.cancerimagingarchive.net/)
- [CBIIT/NBIA-TCIA on GitHub](https://github.com/CBIIT/NBIA-TCIA)

---
Copyright © 2020-2026 Pittsburgh Supercomputing Center. All Rights Reserved.

The [Biomedical Applications Group](https://www.psc.edu/biomedical-applications/) at the [Pittsburgh Supercomputing Center](http://www.psc.edu) in the [Mellon College of Science](https://www.cmu.edu/mcs/) at [Carnegie Mellon University](http://www.cmu.edu).