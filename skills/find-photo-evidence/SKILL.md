---
description: Find photos with permissive licensing related to a given story.
---

You will be given a story title as an argument. Use it to understand the topic and search for relevant photos.

Search the open internet and social media to find photos that are licensed in a way that allows use in this news story. Focus on:

1. Creative Commons licensed images (CC0, CC-BY, CC-BY-SA)
2. Public domain images
3. Government-produced images (which are typically public domain)
4. Wire service or stock photos with open licenses

Store your results as a JSON array in a file called `photo-evidence.json` inside `skill-output/photos/` at the root of the journalism-skills directory, using the story title kebab-cased as the filename. Each entry should have the following fields:

- `url`: direct link to the image or its hosting page
- `description`: what the photo depicts
- `license`: the specific license (e.g., CC-BY-4.0, Public Domain, US Government Work)
- `attribution`: the required attribution text if any
- `source`: where the photo was found (e.g., Wikimedia Commons, Flickr, government website)
- `relevance`: why this photo is relevant to the story

Story title: $ARGUMENTS
