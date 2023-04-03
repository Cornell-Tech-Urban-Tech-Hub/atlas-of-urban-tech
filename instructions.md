# Contributing to the Atlas

## Working with Github

To create a post you will need to have a personal github.com account. Then you can navigate to the [main repository](https://github.com/Cornell-Tech-Urban-Tech-Hub/atlas-of-urban-tech) (or repo) and **_fork_** it. This will create a copy of the repo on your own account. New case studies are added as new folders inside the "cases" folder. You can either add you files through the github web interface (where you can upload the full case study folder and will automatically commit the changes) or use the [github desktop app](https://desktop.github.com/) to copy your repo to edit locally on your computer and then commit and push them to your remote copy.

Once ready you can then issue a pull request to merge your changes back to the main repo. You can choose to keep your local repo if you will continue to make additional edits or close it if submitting final changes.

## Creating A New Case Study

A new case study consists of at minimum a new folder with an plaintext markdown file inside. Case studies should a minimum have one featured image in the folder but is not required to create the initial draft.

View the [example folder](https://github.com/Cornell-Tech-Urban-Tech-Hub/atlas-of-urban-tech/tree/main/cases/example).

First create a folder with the name of the case-study city and iso3 country code in all lower case with spaces represented by dashes (e.g. **new-york-usa**). This folder name must be unique for each case study and will serve as the id and url reference

Inside the folder you will create a markdown (plain text) file called **index.md**. The folder will also contain a featured image for the page heading along with any other images referenced in the case study post.

## Formatting the Markdown File

Each case study markdown file will require a set of metadata (or frontmatter) followed by the body conent in markdown format.

### Metadata / Frontmatter

The metadata is placed at the beginning of the file inside and opening and closing set of three dashes "–––". Each item starts with the identifier followed by a colon and then your case study content and are separated by a line break.

```
---
title: Case Study Template
status: Draft
description: Lorem ipsum dolor sit amet.
city: New York
country_code: US
centroid: [40.712778, -74.006111]
year_start: 2012
year_completed: 2018
featured_image: ./hannah-busing-0V6DmTuJaIk-unsplash.jpeg
featured_desc: New York City Skyline
featured_credit: Hannah Busing (Unsplash)
author: Urban Tech Hub
tags:
- Code
- Markdown
geography: ./example.geojson
geography_caption: Optional Caption for the geograhic information.
---
```

**title**: should be the main title of the case study. Usually the city name

**status**: reflectes the state of the current posts and can reflect three states.

- Draft: Draft post in process
- Review: Ready for review
- Complete: Post ready for publication

**description**: should be a one sentence summary/takaways of the case study. Will serve the page description in metadata and may appear in other areas of the site where the case studies are listed or indexed.

**city**: Should be the city name

**county_code**: Should be the [ISO 3 Letter Country Code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) of the city capitalized

**centroid**: should be the geographic centroid of the case study city/location. For cities the easiest method is to lookup the cities' [wikipedia article](https://en.wikipedia.org/wiki/New_York_City), and click on the coordinates number at the top of the page which will take you to a page with [multiple coordinate formats](<https://geohack.toolforge.org/geohack.php?pagename=New_York_City&params=40_42_46_N_74_00_22_W_region:US-NY_type:city(8804190)>). Copy the "decimal" value which is are two value separated by a comma and place the values inside brackets [40.712778, -74.006111] keeping all six decimal places.

**year_start**: Year the project started

**year_completed**: Year the project was completed. If project is ongoing, leave blank

**featured_image**: should be the filename of the of the feature image for the case study preceeded by a period and forward slash **_./filename.jpeg_** The image should be placed withing the same folder as the markdown file and ideally be a 1920px wide by 1280px tall (landscape) jpeg image. To keep file sizes of the directory managable. To keep the repo size managable do not include files larger than this size and keep the file size under 1mb, please the edit/reduce the file prior to committing them to the repo. **Permission must be recieved for any images included used or they must be creative commons or otherwise rigths cleared**. Services like [unsplash] can be a useful way to find [good images](https://unsplash.com/photos/0V6DmTuJaIk) that are free to use

**featured_desc**: should be short description of what the featured image is showing for alt text and accessibilty

**featured_credit**: should be the credit for the featured image as either the name of the photographer or organization that provided the image. If the image is taken from a site like unsplash or flickr it should be noted in parentheses _Hannah Busing (Unsplash)_
author: Urban Tech Hub

**author**: should be the author of the case study

**tags** should contain any key topic tags listed in markdown list format on the line below.

**geography**: case studies can have an option geojson file to show the project boundary or other key geography formatted as **_./filename.geojson_**. Geojson files can be created or edited from an exisitng geodata format at [geojson.io](https://geojson.io)

**geography_caption**: otional caption for the geojson boundary map.

### Case Study Text

After the frontmatter the body of the markdown file is added. Markdown is written as plaintext with special formatting that gets converted to html formatting.

The body of the case study should follow [this example](https://github.com/Cornell-Tech-Urban-Tech-Hub/atlas-of-urban-tech/blob/main/cases/example/index.md) and the raw plaintext markdown formatting is viewable by clicking on the "raw" button in the github ui or following [this link](https://raw.githubusercontent.com/Cornell-Tech-Urban-Tech-Hub/atlas-of-urban-tech/main/cases/example/index.md)

#### Basic Formatting

An systax guide for markdown can found [here](https://www.markdownguide.org/basic-syntax/) but the most commonly used styles are shown below

headings are formatted with # in front based on the level. Body sections should start at h2 or ## since the the title attribute of the frontmatter/metadata serves as the page title.

```
## Heading 2
### Heading 3
```

basic inline formatting for _italicised_, **bold type**, or **_bold italicised_**

```
_italicised type_
**bold type**
**_bold italicised type_**
```

lists are formatted by starting each line with a number and period (1.) for ordered/numbered list or dashes (-) for unorded lists.

```
Unordered List
- List Item
- List Item

Ordered List
1. List Item
2. List Item
```

linked text is surrounded by brackets with the link url following in parentheses

```
[markdown guide](https://www.markdownguide.org/basic-syntax/)
```

If needed, images can be added inside the body of the markdown file. Please reference the same guidelines for the featured image to ensure permissions are cleared and file size is moderate. Images go inside the same folder. The image alt text (image description) goes inside the brakets and the image title filed follows the image filename in quotes inside the parentheses. This title field is set to be rendered out below the image and should be used for any caption text and the required image credit.

```
![Alt Text / CitiBike Station in New York City](./daniel-adams-URK0rZTiOHc-unsplash.jpeg "Optional Caption Text. Daniel Adams (Unsplash)")
```

---
