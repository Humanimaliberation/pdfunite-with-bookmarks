# pdfunite-with-bookmarks
Merges pdf files **and add pdfbookmarks for each file on level one**.
Original bookmarks will shift one level down.

## Usage
place the file `pdfunite-with-bookmarks` in a directory which is included in PATH e.g. `/usr/bin`.

```bash
pdfunite-with-bookmarks [OPTIONS] INPUTFILE(S) OUTPUTFILE
```
For help call:

```bash
pdfunite-with-bookmarks --help
```

**If you don't need extra pdfbookmarks with filenames** use `pdftk` directly:
```pdftk INPUTFILE(s) cat output OUTPUTFILE``` 
This also merges pdf files and keeps the bookmarks with updated pagenumbers intact.

## Dependencies
- bash
- pdftk
- tput (to use boldfont in terminal)

# References
The script is pretty much an adopted version of steventaitinger's solution shared here:
- https://stackoverflow.com/questions/2969479/merge-pdfs-with-pdftk-with-bookmarks
- https://www.autohotkey.com/board/topic/98985-scripts-to-merge-pdfs-and-add-bookmarks-with-pdftk/
