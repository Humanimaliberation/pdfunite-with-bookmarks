# pdfunite-with-bookmarks
merges pdf files and keeps pdfbookmarks of input files in output file intact with updated pagenumbers.
( Similar to `pdftk INPUTFILE(s) cat output OUTPUTFILE` )

Additionally extra pdfbookmark-entries can be inserted for each file on level 1 
whith titles based on filenames. If used the original bookmarks will shift one level down. 

Without this file-based extra pdfbookmark entry one can also use `pdftk` directly:
```pdftk INPUTFILE(s) cat output OUTPUTFILE``` 
This also merges pdf files and keeps the bookmarks with updated pagenumbers intact.

## Usage
place the file `pdfunite-with-bookmarks` in a directory which is included in PATH e.g. `/usr/bin`.

```bash
pdfunite-with-bookmarks [OPTIONS] INPUTFILE(S) OUTPUTFILE
```
For help call:

```bash
pdfunite-with-bookmarks --help
```

## Dependencies
- bash
- pdftk
- tput (to use boldfont in terminal)

# References
The script is pretty much an adopted version of steventaitinger's solution shared here:
- https://stackoverflow.com/questions/2969479/merge-pdfs-with-pdftk-with-bookmarks
- https://www.autohotkey.com/board/topic/98985-scripts-to-merge-pdfs-and-add-bookmarks-with-pdftk/
