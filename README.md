# MD2HTML

Made for a friend who wanted a standalone .exe that he could click to turn his markdown notes folder into an offline-readable folder of HTML files with embeded / configurable themes.

## Usage

Click on it.  To see terminal output, drag it into your terminal and press enter.

To specify the input, output, and theme folders, run the program with optional folder paths:

`md2html.exe <notesFolder> <htmlDestinationFolder> <themeFolder>`

<br>
<br>

## Config
An optional `config.json` file can be placed in the apps folder.  It can have the following properties:

- `notesFolder` - Absolute path to the folder containing the markdown files.  Leave empty to specify
the folder location in the command line.  If no path is specified, it will default to the executable's `current folder`.

- `htmlDestinationFolder` - The folder where the html files will be saved.  Leave empty to specify
the folder location in the command line.  If no path is specified, it will default to the executable's `current folder/HTML/`.  If no folder exists, it will be created.

- `theme` - The filename of the `.css` theme to use.  Leave empty for no theme.  New themes can be added to the `themes` folder.
  - Current themes include:
    - foghorn
    - modest-dark
    - modest
    - retro
    - simple
    - simple-dark
  - To preview the themes, open `themes/_preview.html` in your browser.

> note: both the config.json and the themes/ folder must be in the same folder as the executable.


## Build from source
To build the executable yourself:
- clone [this repo](https://github.com/FractalHQ/md2html/): `git clone https://github.com/FractalHQ/md2html/`
- install: `npm install`
- build: `npm run build`
> note: you need to have [Deno](https://deno.land) installed to build the executable.
