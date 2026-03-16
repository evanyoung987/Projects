# Language Analysis Tool for Speech Pathology

## 📋 Overview
This tool helps analyze baby speech patterns by marking the first occurrence of each word stem in their utterances. Perfect for completing Speech Language and Hearing Sciences homework!

## 🎯 What It Does
- Reads utterances from a text file (one per line)
- Marks FIRST occurrence of EVERY word with `*^word
- Leaves repeated words unmarked
- Outputs a new text file you can copy into Excel
- Tracks ALL words including "a", "the", "on", "in", etc.

## 💾 What You Need

### Option 1: Run on Your Computer (Recommended)
1. **Python** (free download): https://www.python.org/downloads/
   - Download and install (takes 5 minutes)
   - Windows: Check "Add Python to PATH" during installation
   - Mac: Python may already be installed

### Option 2: Run Online (No Installation)
- Use **Google Colab** (runs in your browser)
- https://colab.research.google.com/

## 📥 How to Get the Code

### Method 1: Download from GitHub
1. Go to the GitHub repository (link will be provided)
2. Click the green "Code" button
3. Click "Download ZIP"
4. Extract the zip file
5. You'll have: `MarkFirstOccurence.py`

### Method 2: Copy the Code
Just copy the `MarkFirstOccurence.py` file provided

## 🚀 How to Use

### Step 1: Prepare Your Input File
1. Open your Excel file
2. Select the "Child Utterance" column (just the utterances, not headers)
3. Copy the cells
4. Open Notepad/TextEdit
5. Paste
6. Save as `utterances.txt`

**Example input file:**
```
a cow.
little boy in there.
up.
yellow.
yellow.
```

### Step 2: Run the Program

#### On Windows:
1. Put `MarkFirstOccurence.py` and `utterances.txt` in the same folder
2. Hold Shift + Right-click in the folder → "Open PowerShell window here"
3. Type: `python MarkFirstOccurence.py utterances.txt`
4. Press Enter

#### On Mac:
1. Put files in same folder
2. Open Terminal
3. Type: `cd ` (with space after cd)
4. Drag the folder into Terminal, press Enter
5. Type: `python3 MarkFirstOccurence.py utterances.txt`
6. Press Enter

#### Double-Click Method (Windows):
1. Create a file named `run.bat` with this content:
```
python language_analysis.py utterances.txt
pause
```
2. Double-click `run.bat`

### Step 3: Get Your Results
- The program creates: `utterances_marked.txt`
- Open this file
- Copy all the text
- Paste into Excel in the "Child Utterance" column

**Example output:**
```
*^a*^ *^cow.*^                          ← First occurrence of "a" AND "cow"
*^little*^ *^boy*^ *^in*^ *^there.*^    ← ALL words are new
*^up.*^                                 ← First "up"
*^yellow.*^                             ← First "yellow"
yellow.                                 ← Repeated, no marker
```

## 📊 How to Complete Your Homework

### # New Word Stems Column:
- Count words with `*^` markers in each utterance
- `*^cow.` = 1 new stem
- `yellow.` (no marker) = 0 new stems

**Example:**
```
Utterance: *^a *^cow.
# New Word Stems: 2

Utterance: yellow.
# New Word Stems: 0

Utterance: *^I *^can *^stand *^on there.
# New Word Stems: 4
```

Note: "there" doesn't have a marker because it appeared earlier in the data.

## 🔧 Customization

### To Change the Marker:
Edit where it says `*^{word}` in the code to use different symbols
Edit where it says `*^{word}` in the code to use different symbols

## 💡 Tips

1. **Keep your input file simple** - one utterance per line, no extra formatting
2. **Don't edit the Python file** unless you want to customize
3. **The output file is safe** - original input is never changed
4. **Run multiple times** - each run creates a fresh output

## 🐛 Troubleshooting

### "Python is not recognized"
- Reinstall Python and check "Add to PATH"
- Or use full path: `C:\Python312\python.exe MarkFirstOccurence.py utterances.txt`

### "File not found"
- Make sure `utterances.txt` is in the same folder as the Python script
- Check the filename exactly matches (including .txt extension)

### Need help?
- Check that Python is installed: Type `python --version` or `python3 --version`
- Make sure you're in the right folder

## 📝 Example Workflow

1. **Monday:** Record baby speech session
2. **Tuesday:** Type utterances into Excel
3. **Wednesday:** Export to `utterances.txt`
4. **Thursday:** Run Python script
5. **Friday:** Copy marked output back to Excel
6. **Saturday:** Count new stems, complete homework! 🎉

## ✅ What You Get

- ✓ Automatic word tracking
- ✓ Clear markers for first occurrences  
- ✓ Easy copy/paste to Excel
- ✓ Progress shown in console
- ✓ Total unique word count
- ✓ Works with any number of utterances

## 📌 Notes

- Case insensitive (Yellow = yellow)
- Handles punctuation automatically
- Preserves original utterance text
- Tracks ALL words including "a", "the", "on", etc.
- Fast processing (100+ utterances in seconds)

---

**Created for Speech Language and Hearing Sciences students**
**Free to use and modify**
