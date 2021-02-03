A group of new user welcome topics to be displayed the first time a newly registered user logs in, or accessible through the help tab on the Galaxy masthead. This is configurable in the galaxy.yml file.

Basic topics include:
    * Data
    * Tools
    * Workflows

The standard version of this repo deployed as the npm package: galaxy_new_user_welcome.

To add/remove topis, alter the list of the new_user_welcome_subjects in the galaxy.yml file.

In order to add topics for specialized instances, clone the repo, add a new topic, and edit the galaxy_new_user_package setting in the galaxy.yml file.

When creating a new topic, the following format is used for the json:

```
    {
        topic: topic title,
        image: image file to be used on the menu for overall topic
        alt: alt text for overall topic image
        blurb: quick desciption of topic
        intro: More in-depth text to be displayed viewing the subtopic options
        subtopics: [
            {
                title: title of subtopic, displayed as card header during the slideshow tour
                header: title of card leading to slideshow tour
                image: image file for the card leading to slideshow tour
                alt: alt text for card image
                intro: Card text about topic
                slides: [
                    [image file for slide, image size [mini-img, small-img, med-img, large-img], slide image alt text, slide main text],
                    ...
                ]
            },
            ...
        ]
    }
```