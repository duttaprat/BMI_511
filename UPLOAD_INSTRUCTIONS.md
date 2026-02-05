# How to Upload Course Materials to GitHub

## 📋 Step-by-Step Instructions

### Option 1: Using GitHub Web Interface (Easiest)

1. **Go to your repository:**
   - Navigate to https://github.com/duttaprat/BMI_511

2. **Create the folder structure:**
   - Click "Add file" → "Create new file"
   - In the name field, type: `2025/02_05_2025/python_programming_tutorial.ipynb`
   - GitHub will automatically create the folders

3. **Upload the notebook:**
   - Copy the content from `python_programming_tutorial.ipynb`
   - Paste it into the file editor
   - Click "Commit new file" at the bottom

4. **Add README files:**
   - Repeat for `2025/02_05_2025/README.md`
   - Repeat for `2025/README.md`
   - Repeat for `README.md` (main repository README)

### Option 2: Using Git Command Line

```bash
# 1. Navigate to your repository folder (or clone it first)
cd /path/to/BMI_511

# 2. Create the folder structure
mkdir -p 2025/02_05_2025

# 3. Copy the files from this folder structure
# You have them in: /home/claude/BMI_511/

# 4. Add all files to git
git add .

# 5. Commit the changes
git commit -m "Add Python programming tutorial for Feb 5, 2025"

# 6. Push to GitHub
git push origin main
```

### Option 3: Using GitHub Desktop (Windows/Mac)

1. **Open GitHub Desktop**
2. **Select your BMI_511 repository**
3. **Copy the folder structure** from the files I created
4. **GitHub Desktop will show the changes**
5. **Write commit message:** "Add Python programming tutorial for Feb 5, 2025"
6. **Click "Commit to main"**
7. **Click "Push origin"**

## ✅ Verify Upload

After uploading, verify that the "Open in Colab" badge works:

1. Go to: https://github.com/duttaprat/BMI_511/blob/main/2025/02_05_2025/python_programming_tutorial.ipynb
2. Click the "Open in Colab" badge at the top
3. The notebook should open in Google Colab

## 🔗 Share with Students

Once uploaded, share these links with students:

### Direct Colab Link:
```
https://colab.research.google.com/github/duttaprat/BMI_511/blob/main/2025/02_05_2025/python_programming_tutorial.ipynb
```

### Repository Link:
```
https://github.com/duttaprat/BMI_511
```

### Specific Date Folder:
```
https://github.com/duttaprat/BMI_511/tree/main/2025/02_05_2025
```

## 📝 What Students Will See

When students click the "Open in Colab" badge:
1. ✅ Notebook opens directly in Google Colab
2. ✅ They can run code immediately
3. ✅ They can save a copy to their Drive
4. ✅ No installation needed!

## 🎯 Benefits of This Setup

- **Easy Access:** One-click to open in Colab
- **Version Control:** All materials in Git
- **Organization:** Clear folder structure by date
- **Professional:** Clean, well-documented repository
- **Shareable:** Simple URLs for students

## 🔄 Adding More Materials Later

For future classes, follow the same pattern:

```
BMI_511/
├── 2025/
│   ├── 02_05_2025/     # Today's tutorial
│   ├── 02_12_2025/     # Next week
│   ├── 02_19_2025/     # Following week
│   └── ...
```

Each date folder should have:
- The notebook file (.ipynb)
- A README.md with description and Colab badge
- Any supporting files (data, images, etc.)

## 💡 Pro Tips

1. **Always test the Colab badge** after uploading
2. **Use descriptive commit messages**
3. **Update the main README** with new materials
4. **Keep notebooks self-contained** (all code works in Colab)
5. **Add comments and documentation** generously

---

Need help? Check GitHub's documentation:
- [Creating files](https://docs.github.com/en/repositories/working-with-files/managing-files/creating-new-files)
- [Uploading files](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)
