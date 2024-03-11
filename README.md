# ComparaBot
A personal project for myself to learn javascript (or most likely, just devolve back to python) for JSON object handling.

## Goal
Make it easy to retrieve updates from https://furrymusicians.info/ 's public API, and check if it's already in my Google Spreadsheet: https://docs.google.com/spreadsheets/d/1m2DREQemi4FSfaBmD-rO6TUnf-iBXLd7-pOHddBKuCg/edit?usp=sharing

## Plan
1. Update local HUGE JSON with this spreadsheet's contents: https://docs.google.com/spreadsheets/d/1m2DREQemi4FSfaBmD-rO6TUnf-iBXLd7-pOHddBKuCg/edit?usp=sharing as pinged by Google Sheets API
2. Get JSON from public API for https://furrymusicians.info/
3. Store both objects as local variables mutated from the original data
4. (Optional) Iterate through furrymusicians.info items with a submission date after the last time this process was run (first run should include all items, then store today's date in a reference file).
5. Iterate through furrymusicians.info JSON. If the name can be found in the HUGE JSON, remove it from the furrymusicians.info JSON variable and continue the loop.
6. Once all items are iterated on, output the remaining items from the https://furrymusicians.info JSON variable. Convert JSON to CSV or other Google Sheets compatible import format.
7. Use Google Sheets API to push result to a new sheet in a file (separate from final destination) for quality checking and to allow further researh on an artist.
8. Manually copy over checked results to the spreadsheet.

## Resources to self

- https://developers.google.com/sheets/api/guides/concepts
- https://api.jquery.com/jQuery.getJSON/
- https://api.jquery.com/jQuery.extend/
