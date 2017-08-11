# Scale Omnibus

## YAML and JSON representations of musical scales

### Description

This repository contains a collections of 399 distinct musical scales under 1012 names, presented in YAML and JSON form.

Fields:
* `"name" [str]`: Name of scale as listed in source material
* `"notes" [int]`: List of offsets from root for each note, in semitones.
* `"intervals" [int]`: List of intervals between adjacent notes, in semitones


Some scales take on different forms whether they are ascending or descending. These scales have the following fields:
* `"name" [str]`: Name of scale as listed in source material
* `"notes_ascending" [int]`: List of offsets from root for each note, in semitones. (Ascending)
* `"notes_descending" [int]`: List of offsets from root for each note, in semitones. (Descending)
* `"intervals_ascending" [int]`: List of intervals between adjacent notes, in semitones. (Ascending)
* `"intervals_descending" [int]`: List of intervals between adjacent notes, in semitones. (Descending)
 
 
The "notes" field is most useful for MIDI processing. For example, to determine the notes that make up a C4 Melodic Minor, add `60 + [0, 2, 3, 5, 7, 9, 11] = [60, 62, 63, 65, 67, 69, 71].`

Scales can be extended to multiple octaves by adding or subtracting multiples of 12, for example `[..., -12, -10, -9, -7, -5, -3, -1, 0, 2, 3, 5, 7, 9, 11, 12, 14, 15, 17, 19, 21, 23, ...]`.


### License and Attribution

All data in this repository was compiled by Francesco Balena in *The Scale Omnibus*, who was gracious enough to release their work for free to the public. Please visit their website at http://www.saxopedia.com/the-scale-omnibus to access the most up-to-date version and support Balena's work.

Converted from *The Scale Omnibus* version 1.02 to YAML and JSON by Corey Hoard.

The Scale Omnibus PDF is licensed under a [Creative Commons Attribution 3.0 Unported License](https://creativecommons.org/licenses/by/3.0/). Please respect this license and attribute Francesco Balena wherever this repository is used.
