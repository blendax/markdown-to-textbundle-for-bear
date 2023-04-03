# Markdown notes to bear notes text bundle

[中文](README_zh.md) [日本語](README_jp.md)

## Environment
- python 3 required
- pip install -r requirements.txt

## Usage
1. `python md-to-bundle.py your-markdown-folder`
2. use subfolder names as tags: `python md-to-bundle.py your-markdown-folder --tags`

exported file will be in `your-markdown-folder-export`

# Known limitations
If you use yaml frontmatter with an empy tag like: `tags:` the program will give an error.
You can remove the empty `tags:`in that file to make it work. Look at the log what file that the converter tries to convert.

# Features
- Copy attachments to the text bundle
- Support obsidian's `![[file]]` format
- Convert `[](markdown.md)` to `[[markdown]]`
- Insert file name(or title in front matter) as title to first line of document (because bear takes first line as title by default)
- Preserve modification time (take modify time from front matter if has one)
- Optionally use subfolder name as tags (with `--tags`)
- Retrieve information from front matter
- Tested apps
    - Obsidian
    - Joplin(exported as Markdown or Markdown + Front Matter)
