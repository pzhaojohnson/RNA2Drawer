# RNA2Drawer

Quickly edit nucleic acid secondary structures and export the drawings as PowerPoint or SVG files. All elements of the drawings (e.g. bases, bonds) are exported as individual PowerPoint or SVG objects, allowing for further manipulation in PowerPoint or Adobe Illustrator. Fonts, colors, and base layout are all customizable in RNA2Drawer, and bases can be colored according to structure probing data (e.g. SHAPE).

<img src="ui2.png">

Questions? See [Frequently Asked Questions](#frequently-asked-questions).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Installation](#installation)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Creating a New Structure](#creating-a-new-structure)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[The Structure Editing Canvas](#the-structure-editing-canvas)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Drawing Styles](#drawing-styles)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[General Drawing Parameters](#general-drawing-parameters)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[The Rigid Drawing Style](#the-rigid-drawing-style)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[The Radial Drawing Style](#the-radial-drawing-style)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Other Customizations](#other-customizations)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Annotating with Structure Probing Data](#annotating-with-structure-probing-data)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Saving Your Work](#saving-your-work)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Exporting Your Drawing](#exporting-your-drawing)<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Frequently Asked Questions](#frequently-asked-questions)

## Installation

### Windows

Download the ZIP file<b>*</b> of the Windows executable for RNA2Drawer [here](https://sourceforge.net/projects/rna2drawer/). Inside the ZIP file will be just a folder named `RNA2Drawer`. You can extract this folder to anywhere on your computer. (A convenient place might be your Desktop.) After you've extracted the folder, enter it. Inside you'll find an Application file named `RNA2Drawer`. Right-click it, highlight `Send to`, and click `Desktop (create shortcut)`. Now you can open RNA2Drawer by just clicking the shortcut on your Desktop.

There might be a delay the first time you open RNA2Drawer as Windows performs a security scan. Windows might also ask you to give permission for the application to run.

<b>*A ZIP file is a compressed file format. Its contents must be extracted (decompressed) before they can be used.</b>

### Mac and Linux

Coming soon ...

## Creating a New Structure

`File` -> `New` allows you to enter a sequence that will be drawn entirely single-stranded, or enter a structure in dot-bracket notation.

`File` -> `Open` allows you to read from a file: <em>i</em>) a sequence, <em>ii</em>) a sequence in FASTA format, <em>iii</em>) a structure in dot-bracket notation, <em>iv</em>) a CT file generated by Mfold, or <em>v</em>) an RNA2Drawer file containing a saved tab.

Make sure that what you enter or the file that you open complies with the parsing steps detailed in the popup windows.

## The Structure Editing Canvas

Each tab of the structure editing canvas contains the drawing of a structure. Clicking a base selects it, and pressing the left and right arrow keys adds/removes neighboring bases from the selection. The structure editing canvas automatically highlights all subsequences that can pair with the currently selected subsequence. Clicking on a pairable subsequence forms the pairing. Alternatively, selecting a set of bases that are already paired and clicking on them will break all base pairs involving those bases.

The bottom bar of the structure editing canvas tells you (from right to left) the sequence range, the current selection, how many pairable subsequences there are, and what clicking the mouse will do.

<b>Multiple tabs can be opened in the structure editing canvas.</b>

## Drawing Styles

RNA2Drawer supports two drawing styles called rigid and radial. Switch between the two in `Drawing` -> `Pick Drawing Style`.

### General Drawing Parameters

These are parameters common to both the rigid and radial drawing styles. Edit these in `Drawing` -> `Edit General Parameters`.

Colors used are the CSS web standards.

&nbsp;&nbsp;&nbsp;&nbsp;`Base` -><br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Base Font`: The font of bases (e.g. Arial Narrow, Times New Roman).<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Base Font Size`: The font size of bases.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Bold Bases`: Toggle to draw bases in bold.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Base Width`: The width of the area allocated to a base.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Base Height`: The height of the area allocated to a base.<br />

Letters in different fonts take up different amounts of space. When changing the font of bases, consider changing `Base Width` and `Base Height` to give bases their needed space.

&nbsp;&nbsp;&nbsp;&nbsp;`Base Pair Bond` -><br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Base Pair Bond Thickness`: The thickness of base pair bonds.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`AU (or AT) Bond Color`: The color AU and AT bonds.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`GC Bond Color`: The color of GC bonds.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`GU (or GT) Bond Color`: The color of GU and GT bonds.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Base Pair Padding`: The gap between a base pair bond and the bases it connects.

&nbsp;&nbsp;&nbsp;&nbsp;`Strand Line` -><br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Strand Line Thickness`: The thickness of strand lines.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Strand Line Color`: The color of strand lines.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Strand Line Padding`: The gap between a strand line and the bases it connects.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Strand Line Threshold`: The minimum distance between two consecutive bases for a strand line to be drawn between<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;them.

&nbsp;&nbsp;&nbsp;&nbsp;`Numbering` -><br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Numbering Font`: The font to numbering (e.g. Arial, Times New Roman).<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Numbering Font Size`: The font size of numbering.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Bold Numbering`: Toggle to draw numbering in bold.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Numbering Color`: The color of numbering.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Numbering Line Length`: The length of numbering lines.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Numbering Line Thickness`: The thickness of numbering lines.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Numbering Line Color`: The color of numbering lines.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Numbering Line Padding`: The gap between a numbering line and the base it is attached to.

### The Rigid Drawing Style

<img src="rigid3.png">

Edit these parameters in `Drawing` -> `Edit Drawing Styles` when you have the rigid drawing style selected.

&nbsp;&nbsp;&nbsp;&nbsp;`Rotation`: The rotation of the drawing.<br />
&nbsp;&nbsp;&nbsp;&nbsp;`Include Base Pair Bonds`: Toggle to draw base pair bonds.<br />
&nbsp;&nbsp;&nbsp;&nbsp;`Base Pair Bond Length`: The length of base pair bonds.<br />
&nbsp;&nbsp;&nbsp;&nbsp;`Minimum Branch Angle`: How squat multibranch loops can be.

### The Radial Drawing Style

A naive radial layout drawing algorithm.

<img src="radial1.png">

<b>The radial drawing style does not prevent base overlaps.</b>

Base overlaps must be resolved by modifying the parameters below. Edit these parameters in `Drawing` -> `Edit Drawing Styles` when you have the radial drawing style selected.

&nbsp;&nbsp;&nbsp;&nbsp;`Rotation`: The rotation of the drawing.<br />
&nbsp;&nbsp;&nbsp;&nbsp;`Base Pair Bond Length`: How long base pair bonds are.<br/>
&nbsp;&nbsp;&nbsp;&nbsp;`Termini Gap Size`: The distance between the 5' and 3' ends of the sequence.<br />
&nbsp;&nbsp;&nbsp;&nbsp;`Joint Angle Range`: The range of angles bulge and internal loops can have.<br />
&nbsp;&nbsp;&nbsp;&nbsp;`Branch Angle Range`: The range of angles that the child stems of a multibranch loop can have.

<b>Typically, reducing the</b> `Joint Angle Range` <b>and</b> `Branch Angle Range` <b>helps to resolve base overlaps.</b>

&nbsp;&nbsp;&nbsp;&nbsp;`Minimum Loop Shift`: The minimum distance between a flexed multibranch loop and its parent stem.<br />
&nbsp;&nbsp;&nbsp;&nbsp;`Minimum Stem Gap`: The minimum distance between two neighboring stems.

Base overlaps between the loops of two neighboring hairpins can be resolved by increasing the `Minimum Stem Gap`.

## Other Customizations

From the `Edit` dropdown menu, you can change:

&nbsp;&nbsp;&nbsp;&nbsp;`Name`: The name of the current tab.

&nbsp;&nbsp;&nbsp;&nbsp;`Sequence Numbering Offset`: The shift in numbering. (Same as in Mfold.)<br />
&nbsp;&nbsp;&nbsp;&nbsp;`Numbering Start`: Determines the position to start labeling the numbering.<br />
&nbsp;&nbsp;&nbsp;&nbsp;`Numbering Interval`: The spacing of numbering labels.

&nbsp;&nbsp;&nbsp;&nbsp;`Base Colors`: Set the colors of bases by position.

&nbsp;&nbsp;&nbsp;&nbsp;`Convert to DNA (Us to Ts)`: Converts all Us to Ts while maintaining all base pairs.<br />
&nbsp;&nbsp;&nbsp;&nbsp;`Convert to RNA (Ts to Us)`: Converts all Ts to Us while maintaining all base pairs.

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

<em>Can I draw DNA instead of RNA?</em> Yes, the popup windows for entering a new structure or opening one from a file allow you to parse the sequence as DNA, and it is possible to convert an existing RNA structure into DNA (see [Other Customizations](#other-customizations)).
