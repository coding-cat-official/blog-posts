# Coding cat public problems

[Coding Cat](https://github.com/tsani/coding-cat) is a simple, in-browser platform for doing small
Python problems to learn programming.

This repository contains the blog posts available on that site.

# Structure of the blog posts

Each blog post must be in its own directory, in the `blogs` subdirectory. The directory name should meaningfully reflect the
problem description, and be named in kebab case.

Each directory must contain the following files to describe the blog post.

- `post.md`
  This is the content of the blog post.
- `meta.json`
  The metadata of the blog post. This is a JSON object with the following keys.
  - `title`: the title of the blog post
  - `author`: the name of the person who wrote the blog post
  - `editor`: (optional) the name of the person/people who edited the blog post
  - `blog_slug`: a unique ID for identifying the blog post. **must be in snake case**
  - `category`: the category of the blog post. For now there is the 'meta' and 'technical' categories
  - `order`: optional field describing the order the posts should be in. If it's not there, they will be shown alphabetically


# Building

Included in this repo is a build script for compiling the list of blogs into `blogs.js`,
which is then imported by the main Coding Cat UI.

- `build-blog` compiles one blog specified as the name of the directory for the blog. This
  produces a `blog.json` file in the blog-posts directory.
- `build-all` compiles all blogs, generating a `blog.json` file
  in each blog directory.
- `build-blogs-list` compiles `blogs.js` in the root directory. This js file imports each
  `blog.json` file for each blog and defines a default export of a list of all the blog objects.
