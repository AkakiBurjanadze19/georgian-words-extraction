# Description
This notebook processes the Wikipedia dump to extract plain Georgian language text and builds a `train/val/test` datasets for a sequence-to-sequence spellchecker.

## Usage
To use this notebook, you need to download the Wikipedia dump from [https://dumps.wikimedia.org/kawiki/latest/](Here). Specifically, you need to download the file that ends with `.bz2` extension.
You also need to install `mwparserfromhell` (`pip install mwparserfromhell`) which is third-party library to parse and strip Media WikiMarkup, leaving only plain text. After all these steps, you are ready
to use this notebook in a project where you have a wikipedia dump file.

## Functions
1. `process_wiki_dump(bz2_file_path, output_txt_path)` - extracts plain Georgian-language text from a Wikipedia XML dump file.
2. `extract_frequent_georgian_words(input_file_path, output_file_path, min_frequency=4)` - builds a filtered Georgian word frequency list from the raw text corpus.
3. `introduce_type(word)` - synthetically generates typos in Georgian words to create training data for the spellchecker.
4. `generate_seq2seq_dataset(dict_path)` - builds the final train/val/test datasets for the seq2seq spellchecker
