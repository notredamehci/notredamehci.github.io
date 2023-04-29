# Website for the Notre Dame HCI group

This is the website hub for Notre Dame HCI group led by [Ronald Metoyer](http://sites.nd.edu/ronald-metoyer/), [Toby Jia-jun Li](https://toby.li/), [Diego Gómez-Zará](https://www.dgomezara.cl/), and [Karla Badillo-Urquiola](https://kbadillou.weebly.com/). The website was built by [Zheng Zhang](http://zhengzhang.me/) and got inspired by [CMU's Data Interaction Group](https://dig.cmu.edu/).

## Run and deploy

The website is deployed on Github Page at this time, any change made to the repo would take effect automatically after a few minutes that pull request gets approved. To run the website on server, please install Jekyll dependencies with `bundle`. Then run `bundle exec jekyll serve --livereload` to start the website page.

## Run with Docker

```
docker run \
  --volume="$PWD:/srv/jekyll" \
  -p 4000:4000 -p 35729:35729 \
  -it jekyll/jekyll \
  jekyll serve --livereload
```

## Add Content

### Add a member

You can take two steps to add a new member under the `people` page:

1. Create a new file named `[last_name]_[first_name].md` for the member under `_people` folder, make sure both last name and first name are lower cased. It ensures that people would appear in an alphbetical order regarding their last name. The file content should follow the format:

```
---
name: [member's name]
website: [personal link]
image: /assets/people/[firstname+lastname].[png/jpg/jpeg/...]
role: Faculty | Graduate Student | Undergraduate | Staff | Visiting Scholar
title: Professor | Associate Professor | Assistant Professor | Postdoctorate | PhD Student | Master Student | Undergraduate | Visiting PhD Student | Visiting Master Student | Visiting Undergraduate | PhD Graduate | ...
alumni_since: [year he/she/they left]
---
```

Note: `alumni_since` property should only be specified when the person has graduated or left, members with this property specified would appear in the `Alumni` section. Also, for undergraduates, it recommends to specify their `title` property as their graduating class (e.g. `Class of 2025`)

2. Add the member's profile image to `assets/people` folder. The name format should be `firstname+lastname.[png/jpg/jpeg/...]`. For example, the name of the profile image for Zheng Zhang should be `zhengzhang.jpg`. Make sure the suffix is line with what you specify in the `image` property in the member's `.md` file.
