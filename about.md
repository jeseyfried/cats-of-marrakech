---
title: About
layout: base
---

# About This Project

For Spring Break in March 2026, I traveled to Marrakech. As my travel buddy and I walked around the medina, I saw cats everywhere and couldn't stop myself from taking pictures of them all.

This site also demonstrates the power of using Copilot with GitHub. I copied the photos into a new folder in assets/images and then Copilot was able to create all the code necessary for making the cat photos into pins on the map. 

## Prompt for Copilot

Here is my prompt and the summary from Copilot of its steps to create the map:

*On this page, please create a card for each of the images in assets/images/marrakech-cats. The card should include geographic location extracted from the metadata of each image. Then edit map.html so that the map uses the newly created cards instead of getting geo location from YAML headers. The overall goal is to have a pin on the map for each of the photos, and when a user clicks on the pin, just the image appears.*

There are about 200 images. I need to extract GPS coordinates from their EXIF metadata. Let me create a Python script to do this.
All 208 images have GPS data extracted successfully. Let me verify the generated YAML file:
Now I'll update the map include to support image-only popups from the data file:
Now I'll make a comprehensive update to support the cat-images data source:
Done! Here's what I implemented:

- Created cat-images.yml - Contains 208 cat images with GPS coordinates extracted from their EXIF metadata
- Updated map.html - Added a new data_source parameter:
        data_source="pages" (default) - Uses page YAML headers (existing behavior)
        data_source="cat-images" - Uses the cat images data file with image-only popups
- Updated index.md - Now uses data_source="cat-images" to display pins for all cat photos

The map now shows a pin for each of the 208 cat photos in Marrakech. When you click a pin, a simple popup appears showing just the cat image. The existing page-based map functionality is preserved for other uses via the data_source parameter.

---

*This site was built with the [Xanthan framework](https://xanthan-web.github.io/xanthan/), a free, open-source toolkit for academic websites hosted on GitHub Pages.*
