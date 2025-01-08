# Welcome to the People listing sub directory

## Understanding the workflow

Each person is an individual listing that is hosted on the `people` page. These are divided into current and past members that are specified in a `YAML` file (`people_current.yml` and `people_past.yml`), and the formatting is handled by the respective `.ejs` files (`assets/ejs/`). 

It is thus important to remain consistent with the white spacing/tabbing as well as using the correct keys (categories). It is not critical that all keys have a value, however at a minimum one should provide the name, description, and email of each new member. 

## The different keys (categories)

Each person also has an associated list of categories (keys) that one can provide information for. Although it is possible to provide nothing else except for the name of a new member for the sake of aesthetics and completeness of information please avoid this.

The categories are provided in the table below, as well as a brief description of the type of information needed

| Key           | Information needed         | Description                                             |
|:--------------|:---------------------------|:--------------------------------------------------------|
| name          | Name of member             | Name of member as they wish for it to appear on website |
| description   | Research description       | A *brief* description of research interests             |
| image         | path to image              | Link to profile pic of member                           |
| email         | email address              | preferred email address (does not have to be @sheff)    |
| github        | username                   | Github username                                         |
| www           | url                        | Link to personal website of member                      |
| twitter       | username                   | Twitter username                                        |
| bluesky       | username                   | Bluesky username                                        |
| orcid         | number                     | ORCiD number                                            |
| googlescholar | Scholar ID                 | Google scholar ID (can be found in url, 12 characters)  |

It is possible to add new categories but this will also need to reflect in the relevanr `.ejs` script...

## Current and past members

New members should be added to `people_current.yml`. When a member leaves the research group they must be moved from the `people_current.yml` to `people_past.yml` file (you do not need to alter any of the information, just cut and paste).

Images for each member should be dropped in the `mugshots/` folder.