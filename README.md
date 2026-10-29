# velcy-chinese-tones

Pinyin tones for Chinese words, as bundled in the VELCY keyboard for iPhone.
The keyboard uses this data to show small tone-marked pinyin (nǐ hǎo, yínháng, māma)
above Chinese candidates. This repository publishes the same data as a plain text table
under **CC BY-SA 4.0**, as required by the license of its source, CC-CEDICT.

## Files

- **`ChineseTones.tsv`** — one simplified-Chinese word per line:
  `word<TAB>reading[ / reading…]`
  - syllables are separated by spaces, each followed by its tone:
    `1`–`4`, `5` = neutral tone, `0` = undecided (the keyboard shows no tone mark)
  - `u:` = ü (e.g. `lu:4 se4` = lǜsè)
  - when a word has more than one reading, the more common one comes first
  - lines starting with `#` are comments
- **`LICENSE`** — the full text of the Creative Commons Attribution-ShareAlike 4.0
  International Public License.

The app contains exactly the same words, syllables and tones (in a binary form).

## Source

Derived from **CC-CEDICT** (https://cc-cedict.org/, maintained by MDBG),
licensed under the Creative Commons Attribution-ShareAlike 4.0 International License.

CC-CEDICT was read from these copies of it:
- word readings: `cc_cedict.txt` of phrase-pinyin-data (https://github.com/mozillazg/phrase-pinyin-data)
- single-character readings: `cc_cedict.txt` of pinyin-data (https://github.com/mozillazg/pinyin-data)

## Changes made to CC-CEDICT

- Kept only the headword (simplified Chinese), pinyin syllables and tones.
  **English definitions, traditional characters and all other fields were removed.**
- Kept only words that the keyboard can produce, plus every single character used in them.
- When CC-CEDICT gives several tone patterns for the same spelling of a word, picked the one that
  matches `pinyin.txt` of phrase-pinyin-data (MIT License); otherwise the syllables that differ
  were set to `0` (undecided).
- For a single character with several tones on the same spelling, used the most customary reading
  from `pinyin.txt` of pinyin-data (MIT License) when it has that spelling; otherwise `0`.
  得 (de) and 过 (guo) are always `0` when they stand alone.
- Erhua 儿 is kept as `er5` (the keyboard writes it as `r`: yìdiǎnr).
  一 and 不 keep their dictionary tones (`yi1`, `bu4`); the keyboard applies tone sandhi
  (bú shì, yí gè) when it displays them.
- Pinyin is lower case (the copies used do not keep capitals for proper nouns).

## License

This data is licensed under the **Creative Commons Attribution-ShareAlike 4.0 International
License** (CC BY-SA 4.0). See [`LICENSE`](LICENSE) or
https://creativecommons.org/licenses/by-sa/4.0/.

When you use it, credit CC-CEDICT (MDBG) and this repository, and share what you make from it
under the same license.

---

## 日本語

VELCY キーボード（iPhone）に入れている、中国語の語の声調のデータです。
キーボードはこのデータで、中文の候補の上に声調記号つきの拼音を小さく出します。

元データは CC-CEDICT（MDBG。CC BY-SA 4.0）。その決まりに従い、アプリに入れたものと同じ中身を
この表（`ChineseTones.tsv`）として、同じ **CC BY-SA 4.0** で公開しています。
英語の意味は入れていません。変えたところは上の「Changes made to CC-CEDICT」のとおりです。
