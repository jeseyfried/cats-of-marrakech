---
title: Template Instructions for Students
layout: base
---

# Getting Started with Your Class Project Site

<style>
/* Page-specific rhythm tuning for long instructional content */
h2 {
   margin-top: 1.6rem;
   margin-bottom: 0.6rem;
}

h3 {
   margin-top: 1.1rem;
   margin-bottom: 0.4rem;
}

p,
ul,
ol {
   margin-bottom: 1rem;
}

hr {
   margin: 1rem 0;
}
</style>

This page guides you through setting up your own project folder in this class project template. Once you've created your folder and added your first page, **you can delete this file**—it's just here to help you get started.

## What You Have

Your instructor has already set up this template with:
- A **homepage** that introduces class projects (`index.md`)
- **Sample essay folders** that show what a finished project looks like
- An **essays folder** structure where you'll add your own project
- All the styling and design already done for you

## Quick Start: Your First Steps

### Step 1: Open the Code Editor in Your Browser

The easiest way to edit your site is using GitHub's built-in code editor. **No need to download anything!**

1. Go to your repository on GitHub
2. Press the **`.` (period) key** on your keyboard
   - This opens VS Code in your browser
   - You'll see all your files on the left side
3. You're now ready to edit!


### Step 2: Create Your Project Folder

Your project needs its own folder. Here's how:

1. In the VS Code sidebar, find the `essays/` folder
2. Right-click on `essays/` and select **"New Folder"**
3. Name your folder using **kebab-case** (lowercase with hyphens, no spaces)
   - ✅ Good examples: `great-fermentation-debate`, `pigeon-conspiracy`, `hot-dog-sandwich`
   - ❌ Bad examples: `Great Fermentation Debate` (spaces), `great_fermentation_debate` (underscores)
4. Press Enter to create the folder

**What your folder structure will look like:**
```
essays/
├── your-project-name/
│   ├── images/           (create this next)
│   └── index.md          (create this next)
```


### Step 3: Create an Images Folder

Inside your new project folder, you need a folder for images:

1. Right-click on your new folder (e.g., `your-project-name/`)
2. Select **"New Folder"**
3. Name it `images`
4. Press Enter


### Step 4: Copy a Sample Index File

Now you need to create your first essay page. You can copy from one of the samples:

1. Look in the `essays/` folder—you'll see sample folders
2. Open one of them and find the `index.md` file inside
3. **Copy the entire contents** (select all the text and copy)
4. Right-click on your project folder and select **"New File"**
5. Name it `index.md`
6. **Paste the sample content** into your new file
7. Save it (Ctrl+S or Cmd+S)

Now you have a starting point! You can edit this file to add your own title, introduction, and content.


## Your First Edits

### Update the Front Matter (Top of Your File)

At the very top of `index.md`, you'll see something like:

```yaml
---
layout: base
title: Your Project Title
---
```

Change the `title` to match your actual project. That's it!


### Add Your Content

Below the `---` lines, replace the sample content with your own writing, analysis, images, etc. Keep the same structure and formatting.


### Add Your Images

1. In VS Code, right-click on your `images/` folder
2. Select **"Upload..."** and choose image files from your computer
3. Once uploaded, you can reference them in your `index.md` file with:
   ```markdown
   ![description]({{ site.baseurl }}/essays/your-project-name/images/image-name.jpg)
   ```

**Image naming tips:**
- Use **lowercase only** (no capitals)
- Use **hyphens** between words, not spaces (e.g., `band-photo.jpg` not `band photo.jpg`)
- Make names **descriptive** (e.g., `stage-setup.jpg` instead of `photo1.jpg`)


## Understanding the Layout

When you look at a sample project, you'll see different "layout" options at the top:

- **`layout: base`** — Simple, clean page with navigation and footer
- **`layout: scrollstory`** — Fancy scrolling effects with background images (more advanced!)
- **`layout: map`** — If your project involves a map or spatial elements

Start with `layout: base` unless your instructor specifies otherwise.


## Editing Your Files

### How to Make Changes

1. Open VS Code in your browser (press `.` key)
2. Click the file you want to edit in the left sidebar
3. Type to make changes
4. Press **Ctrl+S** (or **Cmd+S** on Mac) to save
5. Your changes appear on your website automatically!


### Using Markdown

You don't need to know HTML! Just use simple **markdown** formatting:

```markdown
# This is a heading (H1)

## This is a subheading (H2)

**This text is bold**

*This text is italic*

[This is a link](https://example.com)

- Bullet point 1
- Bullet point 2
- Bullet point 3
```

**Tip:** Look at the sample pages in the `essays/` folder to see examples of markdown you can copy!


## Using AI to Write and Format Your Essay

You don't need to memorize markdown syntax or figure out image tags on your own. AI assistants like Claude or ChatGPT work well with Xanthan because the framework uses named, documented components.

**A useful starter prompt:**

> "I'm working on a class project essay using the Xanthan Jekyll framework. My essay is in `essays/my-project-name/index.md`. Here's the file: [paste your index.md]. I want to add an image on the right side of the text with a caption. The image is at `images/my-photo.jpg`. Can you show me the Xanthan include tag for that?"

Other things AI handles well:
- Drafting or editing your essay text
- Formatting a bibliography in a consistent style
- Fixing broken markdown (paste the problem section and ask what's wrong)
- Explaining what any front matter field or component parameter does

You can also paste your whole essay and ask: "Does this markdown look correct? Are there any formatting issues?"

Start small—ask AI to help with one thing at a time—and you'll build confidence quickly.


## Need Help?

### Ask Your Instructor

If something breaks or doesn't work:
- Let your instructor know
- Tell them what you were trying to do
- Share a screenshot if helpful


### Use AI Tools

You can ask AI assistants like Claude or ChatGPT:
- "How do I add an image to my markdown file?"
- "How do I add a new section to my essay?"
- "What's wrong with this code?" (paste your code and the error)
- "Can you write this text in markdown format?"


### Check your included Docs

For more advanced features:
- Browse the `/docs/` folder in your repository


## When You're Ready to Clean Up
Once you understand how to edit your site and you're happy with your project:

1. **Delete this file** (`instructions.md`)
   - Right-click it in VS Code and select "Delete"
2. **Remove it from navigation** (if your instructor set that up)
3. Keep your project folder and start adding your real content!


---

**Questions?** Ask your instructor or check the [Xanthan documentation](https://xanthan-web.github.io/xanthan/).
