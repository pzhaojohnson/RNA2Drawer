# RNA2Drawer

Quickly edit nucleic acid secondary structures and export the drawings as PowerPoint or SVG files. All elements of the drawings (e.g. bases, bonds) are exported as individual PowerPoint or SVG objects, allowing for further manipulation in PowerPoint or Adobe Illustrator. Fonts, colors, and base layout are all customizable in RNA2Drawer, and bases can be colored according to structure probing data (e.g. SHAPE).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Installation](#installation)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Creating a New Structure](#creating-a-new-structure)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[The Structure Editing Canvas](#the-structure-editing-canvas)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Drawing Styles](#drawing-styles)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Other Customizations](#other-customizations)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Annotating with Structure Probing Data](#annotating-with-structure-probing-data)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Saving Your Work](#saving-your-work)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Exporting Your Drawing](#exporting-your-drawing)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Frequently Asked Questions](#frequently-asked-questions)

## Installation

### Windows

Download the ZIP file<b>*</b> of the Windows executable for RNA2Drawer [here](https://sourceforge.net/projects/rna2drawer/). Inside the ZIP file will just be a folder named `RNA2Drawer`. You can extract this folder to anywhere on your computer. (A convenient place might be your Desktop.) After you've extracted the folder, enter it. Inside you'll find an Application file named `RNA2Drawer`. Right-click it, highlight `Send to`, and click `Desktop (create shortcut)`. Now you can open RNA2Drawer by just clicking the shortcut on your Desktop.

There might be a delay the first time you open RNA2Drawer as Windows performs a security scan. Windows might also ask you to give permission for the application to run.

<b>*A ZIP file is a compressed file format. Its contents must be extracted (decompressed) before they can be used.</b>

### Mac and Linux

Coming soon ...

## Creating a New Structure

`File` -> `New` allows you to enter a sequence that will be drawn entirely single-stranded, or enter a structure in dot-bracket notation.

`File` -> `Open` allows you to read from a file: <em>i</em>) a sequence, <em>ii</em>) a sequence in FASTA format, <em>iii</em>) a structure in dot-bracket notation, <em>iv</em>) a CT file generated by Mfold, or <em>v</em>) an RNA2Drawer file containing a saved tab.

Make sure that what you enter or the file that you open complies with the parsing steps detailed in the popup windows.

## The Structure Editing Canvas

Each tab of the structure editing canvas contains the drawing of a structure. Clicking a base selects it, and pressing the left and right arrow keys adds/removes neighboring bases from the selection. The structure editing canvas automatically highlights all subsequences that can pair with the current selection. Clicking on a pairable subsequence forms the pairing. Alternatively, selecting a set of bases that are already paired and clicking on them will break all base pairs involving those bases.

The bottom bar of the structure editing canvas tells you the sequence range, the current selection, how many pairable subsequences there are, and what clicking the mouse will do.

<b>Multiple tabs can be opened in the structure editing canvas.</b>

## Drawing Styles

The two main drawing styles are rigid and radial.

### The Rigid Drawing Style

Blah blah.

### The Radial Drawing Style

Blah blah.

## Other Customizations

From the `Edit` dropdown menu, you can change:

&nbsp;&nbsp;`Name`: The name of the current tab.

&nbsp;&nbsp;`Sequence Numbering Offset`: The shift in numbering. (Same as in Mfold.)<br />
&nbsp;&nbsp;`Numbering Start`: Determines the position to start labeling the numbering.<br />
&nbsp;&nbsp;`Numbering Interval`: The spacing of numbering labels.

&nbsp;&nbsp;`Base Colors`: Set the colors of bases by position.

&nbsp;&nbsp;`Convert to DNA (Us to Ts)`: Converts all Us to Ts while maintaining all base pairs.<br />
&nbsp;&nbsp;`Convert to RNA (Ts to Us)`: Converts all Ts to Us while maintaining all base pairs.

## Annotating with Structure Probing Data

`Annotate` -> `Structure Probing Data (e.g. SHAPE)` allows you to color bases according to their reactivity in structure probing techniques (e.g. SHAPE). Make sure the file containing your reactivity data complies with the parsing steps detailed in the popup window.

<b>This a versatile feature and can color bases according to any set of values, not just structure probing reactivity data.</b>

## Saving Your Work

You can save a tab as an RNA2Drawer file (with the extension `.rna2drawer`). This is a text file containing all the details of a tab's structure drawing (e.g. fonts, colors, base pairs). Opening an RNA2Drawer file in RNA2Drawer will open the tab exactly as it was when it was saved.

## Exporting Your Drawing

From the `Export` dropdown menu, you can export the dot-bracket notation of the structure currently in the structure editing canvas, or a PowerPoint or SVG file of the drawing itself. All aspects of the drawing (e.g. bases, bonds) will be drawn as PowerPoint or SVG objects, allowing for further manipulation in PowerPoint or Adobe Illustrator.

The popup windows for exporting PowerPoint and SVG files allow you to scale the exported drawing by changing the font size of bases. They also allow you to change the thicknesses of lines, since lines tend to appear thicker in PowerPoint and SVG files than they do in the structure editing canvas.

## Frequently Asked Questions

<em>How do I zoom in and out?</em> This is accomplished by changing the font size of bases in `Drawing` -> `Edit General Parameters` -> `Base`. Bigger font size for zooming in, smaller font size for zooming out.
