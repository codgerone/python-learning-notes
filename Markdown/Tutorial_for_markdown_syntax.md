# Tutorial for Markdown
## Heading
```md
'#' for level-1 heading
'##' for level-2 heading
'###' for level-3 heading
```

## Italic and Bold
```md
*text* to show the text in italic
**text** to show the text in bold
***text*** to show the text in italic & bold
```

## List
### unordered list
```md
- item 1
- item 2
- item 3
```
### ordered list
```md
1. item 1
2. item 2
3. item 3
```

## Code
### inline code
Use **\`inline code\`** to represent inline codes. For example, type **\`python test.py\`** in a sentence, it will look like:

The command `python test.py` is used to run python file in terminal.
### code block
Use **\`\`\`multi-line code\`\`\`** to represent multi-line codes in a code block, and it will look like:

```python
print('hello world!')
print('I'm Meiqi!')
```

> **Note:** *It's allowed to specify the language by following the language type after the fisrt \`\`\`. For example, \`\`\`md, \`\`\`python, \`\`\`bash, \`\`\`json, etc.*

## Link
The syntax to create a link is:
```md
[showing text](URL)
```

For exmaple:

```md
[Google translation](https://translate.google.com/)
```
[Google translation](https://translate.google.com/)

## Picture
The syntax to show a picture is:
```md
![Alt text](Path)
```

For exmaple:

```md
![Sunrise](Sunrise.jpg)
```

![Sunrise](images/Sunrise.jpg)

> **Note:** *Only 'relative path' works, right-click the picture and select **Copy Relative Path** to get the correct path.*

## Blockquotes (Notes and Tips)
To create a blockquote, start a line with symbol **'>'**.
For example:
```md
> Note: this shows how to create a blockquote.
```
> Note: This shows how to create a blockquote.

## Visual Separation

Use **'---'** to create a horizontal rule to achieve visual seperation.

---
