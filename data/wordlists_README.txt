Wordlists (normalized, per-language)

Files:
- english_words.ndjson — 417,002 entries
- spanish_words.ndjson — 636,598 entries

Format: NDJSON (newline-delimited JSON), one object per line:
{
  "w": "<word>",         # token (lowercase, cleaned)
  "lang": "<en|es>",
  "len": <int>,          # character length (Unicode-aware)
  "freq": null,          # placeholder for future frequency info
  "tags": []             # placeholder for designer/game tags (e.g., "kid-basic","animals")
}

Notes:
- English only includes a–z (no apostrophes/numbers); Spanish allows áéíóúüñ.
- Accents are preserved in Spanish.
- Duplicates & non-word tokens removed.
- Kept 2–20 character words to avoid 1-letter junk and ultra-long curios.
- Keeping separate files supports dynamic loading while maintaining a shared schema.
