# Cassette J Card Studio

[日本語](README.md) | [English](README.en.md)

A single-file HTML app for designing cassette tape J-cards (the paper insert for the case). All image processing happens in your browser; no installation is needed.

## How to use

Open [https://eiraruinveil.github.io/Cassette-J-Card-Studio/](https://eiraruinveil.github.io/Cassette-J-Card-Studio/). The app is a single HTML file and all image processing runs in the browser. Use the buttons at the top right to switch between Japanese and English (the choice is saved).

Repository: [https://github.com/EiraRuinveil/Cassette-J-Card-Studio](https://github.com/EiraRuinveil/Cassette-J-Card-Studio)

## Templates (styles)

Choose between two J-card styles with the “Style” selector in the toolbar. Both are 300 DPI.

| Style | Total size | Rear flap | Spine | Main (front cover) |
| --- | --- | --- | --- | --- |
| Short flap | 1053 × 1218 px (89.2 × 103.1 mm) | 177 px (15.0 mm) | 153 px (13.0 mm) | 723 px (61.2 mm) |
| Long flap | 1219 × 1200 px (103.2 × 101.6 mm) | 300 px (25.4 mm) | 150 px (12.7 mm) | 769 px (65.1 mm) |

- The short-flap style fits the narrow retaining flap of the case; the flap mainly holds the card in place.
- The long-flap style is the standard J-card; the flap is wide enough to print a track list on.
- The front and back are two sides of the same sheet. The front runs “flap | spine | main” and the back runs “main | spine | flap”, so when folded, the spines meet and the flaps meet.
- Switching styles keeps your design; text and image layer positions are rescaled proportionally. The chosen style is saved in the browser and in project files.

### Template files

Starter templates with labeled panels are provided, handy for test prints. You can load them directly from the “Templates” buttons in card 5 of the app, or download a file below and open it via “Load project”.

[Short-flap template](jcard_shortflap_front_.json)

[Long-flap template](jcard_longflap_front_.json)

## Controls

### Panels

- The panels are the front cover / back main, the spine, and the rear flap, on both the front and back sides.
- Each panel has its own background color and image. Images can be fitted (show whole / fill / stretch), scaled and rotated, and dragged on the preview to position them.
- Type into “Add text to this panel” in card 1 to place text at the center of the selected panel (Enter for line breaks; the Add button or Ctrl+Enter to add). Double-clicking the preview also selects a panel and moves focus to the text box.

### Spine

- Enter the title, artist name and catalog number.
- Title, artist and catalog number each have their own size, font and position (the color is shared across the spine). The direction is rotated, reading bottom-up or top-down.
- The artist and title are shown on one line centered across the spine. Letter spacing is adjustable.
- Spine text can be dragged directly on the preview (along the spine only; it stays centered across the spine). When selected, the ↑↓ keys move it too.
- “Fill the spine area” overlays a color on the spine background (applied to the spines on both sides, with the text drawn on top). To change the spine's own background color, select the Spine panel in card 1.

### Layers (text, images, fonts)

- Text layers: multiple lines, vertical stacking, rotation, letter spacing, color, weight and font, each set individually.
- Image layers: place an image anywhere; adjust its size, rotation, opacity and stacking order.
- Load a font file (TTF / OTF / WOFF / WOFF2) to use it for the spine, text layers and the track list. Loaded fonts are saved in the project file too.
- Layers can be dragged on the preview and clicked to select. Shift+drag moves in a straight line; arrow keys nudge by 1px (Shift+arrows = 10px).
- Click a slider's value label to type a number directly (Enter to confirm, Esc to cancel).

### Track list

- Choose where it goes: the back main panel, the rear flap on the back, or the rear flap on the front.
- Set the text size, letter spacing, color, font and rotation (−180 to 180°). On a flap, a smaller text size fits better; a 90° rotation reads along the flap.
- Typing text turns it on automatically and switches the preview to the side it is placed on.

### Other

- “Both-sides preview” shows the front and back side by side.
- Adjust the preview zoom with “Fit to screen” or the slider.

## Export

In the Export dialog, choose the format and contents. Changing the selection updates the layout preview automatically.

- **Formats**: PDF / PNG / JPG / Print
- **Contents**: card size (front / back / both sides) or A4 (front / back / both sides)
- On A4 you can place two copies of the same design on one page. The dashed cut guides are drawn inverted, so they appear white on dark designs and black on light ones (can be turned off).
- With “Fold lines (panel borders)” set to Include, inverted dashed fold lines are also drawn in exports and prints (and shown in the preview). The setting is saved.
- File names include the dimensions (e.g. `jcard_front_1053x1218_300dpi.png`), which follow the selected style.

## Saving projects

“Save project” stores the images, text, settings, loaded fonts and the selected style in a single JSON file. Open it later with “Load project” to restore everything.

## About printing

- On a home printer, set the print scale to “Actual size” or 100%. Browser printing tends to come out about 0.5mm larger, so the size adjustment starts at −0.5mm; if the size is off, adjust “Size adjustment (mm)”.
- When sending data to a print shop, please check their data preparation guide.
- Depending on the printer, the app, the PDF viewer and the print shop's settings or specifications, actual-size printing may not be possible. The provider of this app is not responsible for print results.
