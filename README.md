# HuRIC

This filesystem collects the whole HuRIC corpus, a collection of robotics commands.

It is composed of 2 versions, one for each language:

* `en`: the Engligh version of HuRIC
* `it`: the Italian verison of HuRIC

In each version, several resources are available:

* `audio_files`: this folder contains all the audio files, grouped by dataset name (e.g. `Robocup`). Moreover, two additional descriptors are included:
	* `db.csv`: required to import the corpus into the HuRIC DAP
	* `mapping.csv`: defines a mapping between the audio file and one (or more) XDG
* `datasets`: basic version of the annotations (i.e. without semantic maps), expressed through the XDG formalism. The lower lever defines the version of the dataset (e.g. `2.0`). Then, the examples are grouped by dataset name (e.g. `Robocup`).
* `huric_export`: the exportable version of HuRIC. Each example is expressed in `hrc` that is a markup language. The lower level defines the version of the dataset (e.g. `2.0`). Then, the examples are grouped by dataset name (e.g. `Robocup`).
* `perceptual_datasets`: perceptual version of the annotations (i.e. with semantic maps), expressed through the XDG formalism. The lower lever defines the version of the dataset (e.g. `2.0`). Then, the examples are grouped by dataset name (e.g. `Robocup`).