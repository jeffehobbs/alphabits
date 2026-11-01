# alphabits

A word-guessing game: guess the letters of a set of related words, with a hint describing how they relate. Live at https://jeffehobbs.github.io/alphabits/

Puzzles are static JSON files in `puzzles/`. The page picks one at random using `puzzles/index.json`. If you add or remove puzzles, rebuild the index:

```
python3 -c "import os,json; json.dump(sorted(f for f in os.listdir('puzzles') if f.endswith('.json') and f!='index.json'), open('puzzles/index.json','w'))"
```
