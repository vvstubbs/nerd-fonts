# Inconsolata

Open-source Monospace Font for code listings by Raph Levien

## Changelog v.2.011

March 2018 glyph set expansion was complete by @appsforartists, which included:

- [x] Glyph Set expanded to include ligatures for ===, !==, =>, <=, >=, ->, <-

## Changelog v.2.001

August 2016 glyph set expansion was complete by Alexei Vanyashin ( [Cyreal][5] ), which included:

- [x] Glyph Set expanded to GF Latin Pro
- [x] Additional glyphs ⊕↑↗→↘↓↙←↖↔↕⇧⇨⇩⇦⬆⮕⬇⬅●○◆◇☹☺☻♠♣♥♦✓✔✕✗✘␣⎋⌂⇪⌧⌫⌦⌥⌘⏎�
- [x] Minor design improvements (trademark corner spurs)

Further reading: Inconsolata expansion project thread on [Google Fonts Discussions][6]

#### Supported glyphs sets:

* GF Latin Pro

![Inconsolata Preview](documentation/img/inco-preview.png)

## License

This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is copied below, and is also available with a FAQ at:
[http://scripts.sil.org/OFL][4]

----

## Inconsolata Build Instructions



### Source Files

Inconsolata source files are available in `.glyphs` format located in the `/sources` directory.

### Font Export options

* TTF and OTF files should be exported into `/fonts/ttf` and `/fonts/otf` folders.

* `TTFs` should be generated from Glyphs App with `Autohint` option checked. At the moment there is no custom build script required to produce font files, since default TTFautohinting options suffice.

![Font Export Options](documentation/font-export.png)

* `OTFs` should be generated with these options:
	* [X] Remove Overlap
	* [X] Autohint
  * [ ] Save as TTF
	* [X] Export destination: $REPO_PATH/fonts/otf

----

## Copyright

Copyright 2006 The Inconsolata Project Authors

## Links

* [Inconsolata on Google Fonts][1]
* [Inconsolata on Levien.com][2]
* [Official Upstream on git][3]

[1]: https://fonts.google.com/specimen/Inconsolata
[2]: http://levien.com/type/myfonts/inconsolata.html
[3]: https://github.com/google/fonts/tree/master/ofl/inconsolata
[4]: http://scripts.sil.org/OFL
[5]: http://cyreal.org
[6]: https://groups.google.com/forum/#!searchin/googlefonts-discuss/inconsolata%7Csort:relevance/googlefonts-discuss/wgVuOx9yo5k/2QSUQ78CCQAJ

## Which font?

### TL;DR

* Pick your font family and then select from the `'complete'` directory.
  * If you are on Windows pick a font with the `'Windows Compatible'` suffix.
    * This includes specific tweaks to ensure the font works on Windows, in particular monospace identification and font name length limitations
  * If you are limited to monospaced fonts (because of your terminal, etc) then pick a font with the `'Mono'` suffix.
    * This denotes that the Nerd Font glyphs will be monospaced not necessarily that the entire font will be monospaced

### Ligatures

By the *Nerd Font* policy, the variant with the `'Mono'` suffix is not supposed to have any ligatures.
Use the non-*Mono* variants to have ligatures.

### Explanation

Once you narrow down your font choice of family (`Droid Sans`, `Inconsolata`, etc) and style (`bold`, `italic`, etc) you have 2 main choices:

#### `Option 1: Download already patched font`

 * download an already patched font from the `complete` folder
   * This is most likely the one you want. It includes **all** of the glyphs from all of the glyph sets. Only caution here is that some fonts have glyphs in the _same_ code point so to include everything some had to be moved to alternate code points.

#### `Option 2: Patch your own font`

 * patch your own variations with the various options provided by the font patcher (see each font's readme for full list of combinations available)
   * This is the option you want if the font you use is _not_ already included or you want maximum control of what's included
   * This contains a list of _all permutations_ of the various glyphs. E.g. You want the font with only [Octicons][octicons] or you want the font with just [Font Awesome][font-awesome] and [Devicons][vorillaz-devicons]. The goal is to provide every combination possible in this folder.


For more information see: [The FAQ](https://github.com/ryanoasis/nerd-fonts/wiki/FAQ-and-Troubleshooting#which-font)


[vim-devicons]:https://github.com/ryanoasis/vim-devicons
[vorillaz-devicons]:https://vorillaz.github.io/devicons/
[font-awesome]:https://github.com/FortAwesome/Font-Awesome
[octicons]:https://github.com/primer/octicons
[gabrielelana-pomicons]:https://github.com/gabrielelana/pomicons
[Seti-UI]:https://atom.io/themes/seti-ui
[ryanoasis-powerline-extra-symbols]:https://github.com/ryanoasis/powerline-extra-symbols
[SIL-RFN]:http://scripts.sil.org/cms/scripts/page.php?item_id=OFL_web_fonts_and_RFNs#14cbfd4a


## Variations (Combinations)

> The combinations and total number of combinations are provided here for reference if you want to create your own variation of a patched Nerd Font.

### Why aren't all variations included ?

Combinations are no longer included by default because of the large inflation in size it caused the Repository _and_ the amount of time it takes to rebuild all of the combinations. This issue would exponentially get worse as the numbers of Fonts and Glyph Sets provided increase.


```sh
# 4094 Possible Combinations:

./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --octicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesome
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --octicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --windows
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --octicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesome
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --octicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs --material
./font-patcher Inconsolata-Regular.ttf  --powerline --use-single-width-glyphs
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --octicons
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesome
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --octicons
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --windows --material
./font-patcher Inconsolata-Regular.ttf  --powerline --windows
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --octicons
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesome
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --octicons
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontlogos
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --powerline --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerline --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerline --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerline --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerline --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerline --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerline --weather
./font-patcher Inconsolata-Regular.ttf  --powerline --material
./font-patcher Inconsolata-Regular.ttf  --powerline
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --octicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontlogos
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesome
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --octicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontlogos
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --windows
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --octicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontlogos
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesome
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --octicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontlogos
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --pomicons
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --powersymbols
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --weather --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --weather
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs --material
./font-patcher Inconsolata-Regular.ttf  --use-single-width-glyphs
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --octicons
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontlogos
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --pomicons
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesome
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --windows --octicons --material
./font-patcher Inconsolata-Regular.ttf  --windows --octicons
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontlogos
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --windows --pomicons
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --windows --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --windows --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --windows --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --windows --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --windows --powersymbols
./font-patcher Inconsolata-Regular.ttf  --windows --weather --material
./font-patcher Inconsolata-Regular.ttf  --windows --weather
./font-patcher Inconsolata-Regular.ttf  --windows --material
./font-patcher Inconsolata-Regular.ttf  --windows
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --octicons
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontlogos
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --pomicons
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesome --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesome --material
./font-patcher Inconsolata-Regular.ttf  --fontawesome
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontlogos
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --octicons --pomicons
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --octicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --octicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --octicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --octicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --octicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --octicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --octicons --weather
./font-patcher Inconsolata-Regular.ttf  --octicons --material
./font-patcher Inconsolata-Regular.ttf  --octicons
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --pomicons
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --fontlogos --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontlogos --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontlogos --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos --weather
./font-patcher Inconsolata-Regular.ttf  --fontlogos --material
./font-patcher Inconsolata-Regular.ttf  --fontlogos
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --pomicons --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --pomicons --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --pomicons --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --pomicons --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --pomicons --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --pomicons --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --powersymbols
./font-patcher Inconsolata-Regular.ttf  --pomicons --weather --material
./font-patcher Inconsolata-Regular.ttf  --pomicons --weather
./font-patcher Inconsolata-Regular.ttf  --pomicons --material
./font-patcher Inconsolata-Regular.ttf  --pomicons
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --powersymbols
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --weather --material
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --weather
./font-patcher Inconsolata-Regular.ttf  --powerlineextra --material
./font-patcher Inconsolata-Regular.ttf  --powerlineextra
./font-patcher Inconsolata-Regular.ttf  --fontawesomeextension --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesomeextension --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesomeextension --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --fontawesomeextension --powersymbols
./font-patcher Inconsolata-Regular.ttf  --fontawesomeextension --weather --material
./font-patcher Inconsolata-Regular.ttf  --fontawesomeextension --weather
./font-patcher Inconsolata-Regular.ttf  --fontawesomeextension --material
./font-patcher Inconsolata-Regular.ttf  --fontawesomeextension
./font-patcher Inconsolata-Regular.ttf  --powersymbols --weather --material
./font-patcher Inconsolata-Regular.ttf  --powersymbols --weather
./font-patcher Inconsolata-Regular.ttf  --powersymbols --material
./font-patcher Inconsolata-Regular.ttf  --powersymbols
./font-patcher Inconsolata-Regular.ttf  --weather --material
./font-patcher Inconsolata-Regular.ttf  --weather
./font-patcher Inconsolata-Regular.ttf  --material
```