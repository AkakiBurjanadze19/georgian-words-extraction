# Description
This notebook processes the Wikipedia dump to extract plain Georgian language text and builds a `train/val/test` datasets for a sequence-to-sequence spellchecker.

## Usage
To use this notebook, you need to download the Wikipedia dump from [https://dumps.wikimedia.org/kawiki/latest/](Here). Specifically, you need to download the file that ends with `.bz2` extension.
You also need to install `mwparserfromhell` (`pip install mwparserfromhell`) which is third-party library to parse and strip Media WikiMarkup, leaving only plain text. After all these steps, you are ready
to use this notebook in a project where you have a wikipedia dump file.
