# Images folder

Just drop your photos in here (e.g. trip1.jpg, concert.png, beach.jpeg ...).
Any .jpg, .jpeg, .png, .gif, .webp, or .avif file works — no renaming needed.

## How it works
The gallery section on the page automatically fetches the list of files in
this folder using the GitHub API, so as soon as you push new images to your
repo, they'll show up in the slideshow and grid — no code changes needed.

## One-time setup
Open `index.html`, find this block near the bottom (inside the <script> tag):

```js
const GH_USER = "abhishek-gupta420";
const GH_REPO = "portfolio";          // <-- change to your actual repo name
const GH_BRANCH = "main";             // <-- change if your default branch is "master"
```

Make sure `GH_REPO` matches the exact name of the GitHub repository you
publish this site from, and `GH_BRANCH` matches its default branch.

## Notes
- This only works once the site is hosted on GitHub (the GitHub API can't be
  reached when opening index.html locally as a file).
- The repo must be public for the API to return the file list without
  authentication.
- Images are sorted alphabetically — prefix filenames with numbers
  (01-beach.jpg, 02-mountains.jpg) if you want a specific order.
