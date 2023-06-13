# Americana Fonts

<img src="doc-img/osm-americana-logo.png" alt="Americana map style logo" width="200"/>

The Americana fontstack is built from [Google Fonts](https://fonts.google.com/). The name "fontstack66" is a nod to [Historic Route 66](https://www.nps.gov/subjects/travelroute66/index.htm).

## Usage

```json
glyphs: "https://osm-americana.github.io/fontstack66/{fontstack}/{range}.pbf"
```

Then, in a maplibre-gl stylesheet, you can use the packaged fonts like such:

```json
"text-font": ["Americana-Bold"]
```

## Contributing

In order to add fontstack support, modify the `fonts.json` file as follows:

1. Add font-family and variant information to the `font-families` section. The font-family is the name of the font as listed on Google Fonts, e.g. "Noto Sans". Use `gfi download "<name of font>"` to get a full list of the variants. The variant is everything to the right of the dash in the filename, so if a file is named `NotoSans-700.ttf`, the variant is `700`, though it will be listed in Google as something like "Bold 700". The `gfi` command requires you to install the `google-font-installer` package into npm with `npm install -g google-font-installer`.
2. Define the range of characters that you want rendered in this font in the `glyph-ranges` section. Since this is JSON, you'll have to convert hex to decimal here. The named parameter is simply a name that is used in the rest of the file to refer to this range of characters. This is an _inclusive_ range so for example `[0, 255]` will include codepoint 0 and codepoint 255.
3. The `custom-font-stacks` section lists each font-stack and which font/glyph range combinations should be included in that fontstack.
4. The `bundle-font-stacks` section lists all font stacks which should be bundled in their original form.

## Provided Fonts

The following fonts are provided:

- Americana - based on Noto Sans Regular, generally 400 weight
- Americana-Bold - based on Noto Sans Regular, generally 700 weight
- Americana-Italic - an italic version of Americana
- Americana-Bold-Italic an italic version of Americana-Bold
- [Noto Sans HK](https://fonts.google.com/noto/specimen/Noto+Sans+HK) - Hong Kong Han ideograms
- [Noto Sans JP](https://fonts.google.com/noto/specimen/Noto+Sans+JP) - Hiragana, Katakana and Kanji
- [Noto Sans KR](https://fonts.google.com/noto/specimen/Noto+Sans+KR) - Hangul and the Korean Hanja scripts
- [Noto Sans SC](https://fonts.google.com/noto/specimen/Noto+Sans+SC) - Simplified Chinese variant of the Han ideograms.
- [Noto Sans TC](https://fonts.google.com/noto/specimen/Noto+Sans+TC) - Traditional Chinese variant of the Han ideograms
