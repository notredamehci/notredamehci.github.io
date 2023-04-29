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

To add specific content, follow the README guides in the corresponding directories:

* [Add a person](_people)
* [Add a publication](_publications)
* [Add a post](_posts)
