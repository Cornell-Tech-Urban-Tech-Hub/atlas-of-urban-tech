# Atlas of Urban Tech

A global atlas of case studies of tech-enabled urban districts and municipal digital masterplans created by the Jacobs Urban Tech Hub at Cornell Tech.

This content will be published at [https://www.atlasofurbantech.org](https://www.atlasofurbantech.org).


## Contributing to the Atlas

### 1. Fork the Repo

To create a post you will need to have a personal github.com account. Then you can navigate to the [main repository](https://github.com/Cornell-Tech-Urban-Tech-Hub/atlas-of-urban-tech) (or repo) and **_fork_** it. This will create a copy of the repo on your own account. New case studies are added as new folders inside the "cases" folder. You can either add you files through the github web interface (where you can upload the full case study folder and will automatically commit the changes) or use the [github desktop app](https://desktop.github.com/) to copy your repo to edit locally on your computer and then commit and push them to your remote copy.

Once ready you can then issue a pull request to merge your changes back to the main repo. You can choose to keep your local repo if you will continue to make additional edits or close it if submitting final changes.

### 2. Create A New Case Study

A new case study consists of at minimum a new folder with an plaintext markdown file inside. Case studies should a minimum have one featured image in the folder but is not required to create the initial draft. View the [example folder](https://github.com/Cornell-Tech-Urban-Tech-Hub/atlas-of-urban-tech/tree/main/templates/case).

Create a new folder inside the `/cases` folder, with the name of the case-study city and iso3 country code in all lower case with spaces represented by dashes (e.g. ```new-york-usa```). This folder name must be unique for each case study and will serve as the id and url reference.

Copy the contents of the `/templates/case` folder into this new folder. You will replace the content in this template folder with your own:

- A markdown (plain text) file containing metadata, formatted text, and inline image references. (```index.md``` )
- A featured image for the page heading along with any other images referenced in the case study post. (in the template file, ```daniel-adams-URK0rZTiOHc-unsplash.jpeg``` and ```hannah-busing-0V6DmTuJaIk-unsplash.jpeg``` )
- A geojson file describing the approximate geogrpahic boundary of your case study municipality or district (in the template ```example.geojson```, but you should rename yours using the same city-country string you used for the folder name)

Inside the folder you will create a markdown  called **index.md**. 

### 3. Fill in Case Study Metadata

Each case study markdown file must iclude a metadata section that provides the site renderer with basic information used to generate the web pages.

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
- Mobility
- Energy
geography: ./example.geojson
geography_caption: Optional Caption for the geographic information.
---
```

#### Required Fields
- **title**: The main title of the case study. Usually the plan or district name (e.g. "New York City Internet of Things Plan" or "Songdo International Business District")

- **status**: The state of the case study. Leave your case in `Draft` while composing and change to `Review` when it is merged into the main repo (See below). Do not use `Complete`—this is for the instructor to publish your case to the website.

        - Draft: Draft post in process
        - Review: Ready for review
        - Complete: Post ready for publication

- **description**: A one sentence summary/takaways of the case study. Will serve the page description in metadata and may appear in other areas of the site where the case studies are listed or indexed.

- **city**: The city name.

- **county_code**: Tthe [ISO 3 Letter Country Code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) of the city capitalized

- **centroid**: The geographic centroid of the case study city/location formatted as lat, lon enclosed in ```[brackets]```. For cities the easiest method is to lookup the cities' [wikipedia article](https://en.wikipedia.org/wiki/New_York_City), and click on the coordinates number at the top of the page which will take you to a page with [multiple coordinate formats](<https://geohack.toolforge.org/geohack.php?pagename=New_York_City&params=40_42_46_N_74_00_22_W_region:US-NY_type:city(8804190)>). Copy the "decimal" value which is are two value separated by a comma and place the values inside brackets [40.712778, -74.006111] keeping all six decimal places.

- **year_start**: Year the project started.

- **year_completed**: Year the project was completed. If project is ongoing, leave blank.

- **featured_image**: The filename of the of the feature image for the case study preceeded by a period and forward slash **_./filename.jpeg_** The image should be placed withing the same folder as the markdown file and ideally be a 1920px wide by 1280px tall (landscape) jpeg image. To keep file sizes of the directory managable. To keep the repo size managable do not include files larger than this size and keep the file size under 1mb, please the edit/reduce the file prior to committing them to the repo. **Permission must be recieved for any images included used or they must be creative commons or otherwise rigths cleared**. Services like [unsplash] can be a useful way to find [good images](https://unsplash.com/photos/0V6DmTuJaIk) that are free to use

- **featured_desc**: A short description of what the featured image is showing for alt text and accessibilty, no more than 20 words.

- **featured_credit**: The credit for the featured image as either the name of the photographer or organization that provided the image. If the image is taken from a site like unsplash or flickr it should be noted in parentheses ```_Hannah Busing (Unsplash)_```.

- **author**: The author of the case study, e.g. you the student.

- **tags** Up to three tags from the following taxonomy, one per line, preceded by a hyphen:

        Mobility
        Buildings
        Energy
        Environment
        Food
        CivicTech
        InnovationSystems
        InformationSystems
        HealthEducation

- **geography**: A geojson file indicating the project boundary or other key geography formatted as **_./filename.geojson_**. Geojson files can be created or edited from an exisitng geodata format at [geojson.io](https://geojson.io).

- **geography_caption**: A brief caption for the geojson boundary map.

### 4. Write Your Case Study Content

After the frontmatter the body of the markdown file is added. Markdown is written as plaintext with special formatting that gets converted to html formatting. An syntax guide for markdown can found [here](https://www.markdownguide.org/basic-syntax/).

The following sections are required:

- **Overview**. A 100 to 150 word summary of the case study.
- **Key Characteristics**.  Summarize the most visible essential characteristics of the project. For districts: How does the district employ 3-5 of the key characteristics of New Century Cities? For plans: How does the plan address each of the three activities (development, engagement, implementation) of the digital masterplanning process described in the 2015 Townsend and Lorimer paper?
- **Goals and Aspirations**. Summarize the most important goals of the project. Replace the placeholder title with a succinct name for the goal. The text should be around 50 words.
- **Technology Interventions**. Identify 3-5 specific technology-enabled interventions the project employs or proposes. The text should be around 75-125 words. Separate into more than 1 paragraph as needed. This is a good place to insert additional images, be sure to include captions identifying the source and make sure to not use copyrighted images.
- **Stakeholders**. Identify 3-5 key stakeholder organizations or groups. The text should be around 50 words, and include a link to the organization.
- **Leadership**. Conduct one interview with a project leader, and link to a LinkedIn or other profile. Provide a brief biography, no more than 75 words. Identify 3-5 insights or themes from the interview. Feel free to add a photo of the individual here.
- **Financing**. Identify at least one financing scheme being used in this project or plan. About 100 words is probably a good length for this.
- **Outcomes**. Identify 3-5 (anticipated) outcomes. What will/has the project achieved? Thes should not be the same or repeated from elsewhere. Use this space to emphasize something different. About 50 words per is minimum, but these can be as long as you want/need. 
- **Open Questions**. Identify 1-3 open question(s). What is uncertain, unclear, or still unresolved about this project? These can be 50 words or less
- **References**. This should have 2 sections, primary and secondary sources.
    - Primary Sources: 3-5 project plans, audits, reports, etc.
    - Secondary Sources: 5-7 secondary source documents: news reports, blog posts, etc

        ### Primary Sources

        <!--  -->

        - Create a list by starting a line with `+`, `-`, or `*`
        - Sub-lists are made by indenting 2 spaces:
        - Very easy!

        ### 

        <!-- .. -->

        - Create a list by starting a line with `+`, `-`, or `*`
        - Sub-lists are made by indenting 2 spaces:
        - Very easy!


These sections are all included in the example [index.md](https://github.com/Cornell-Tech-Urban-Tech-Hub/atlas-of-urban-tech/blob/main/cases/example/index.md) that you copied from the ```templates/case``` folder to create your case study. Simply replace the dummy text and links with your own.


### 4. Add Images and Links

#### Links

Sections of text can be hyperlinked to external resources using Markdown. To create a link like this, use thecode below --> [Anthony Townsend's LinkedIn]("https://www.linkedin.com/in/anthony-townsend-2344b9212/")

```
[Anthony Townsend's LinkedIn]("https://www.linkedin.com/in/anthony-townsend-2344b9212/")
```

#### Images

In addition to the rquired featured image referenced in the metadata (and only there), additional images can be added inside the body of the markdown file (at least one per technology intervention is reqiured). Please reference the same guidelines for the featured image to ensure permissions are cleared and file size is moderate. Images go inside the same folder. The image alt text (image description) goes inside the brakets and the image title filed follows the image filename in quotes inside the parentheses. This title field is set to be rendered out below the image and should be used for any caption text and the required image credit.

```
![Alt Text / CitiBike Station in New York City](./daniel-adams-URK0rZTiOHc-unsplash.jpeg "Optional Caption Text. Daniel Adams (Unsplash)")
```

### 5. Create Your Map

We will spend a session in class on how to create the GeoJSON file to describe your case study area.

### 6. Commit, Push, and Merge Your Contribution

The final step is to commit and push your changes to the fork, then submit a pull request to have your changes merged to the main repo.



## License

 <p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/Cornell-Tech-Urban-Tech-Hub/atlas-of-urban-tech">Atlas of Urban Tech</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://urban.tech.cornell.edu/">Jacobs Urban Tech Hub, Cornell Tech</a> is licensed under <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-NC-SA 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1"></a></p>

