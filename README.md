# MLflow Website

This is the website for the MLflow project, built on an open source Jekyll theme called [Hydra](https://github.com/CloudCannon/hydra-jekyll-template).

# Building

Use the `bundle` command to run jekyll commands 

And when you're building to push to production use:

`JEKYLL_ENV=production bundle exec jekyll build`

...this will ensure that the sitemap and robots.txt is built correctly and that the google analytics snippet gets inserted into the pages.

# Deploying

We use `s3_website`, which you can install via `gem install s3_website` -- see https://github.com/laurilehmijoki/s3_website

Make sure you have your aws credentials set up (probably via `aws credentials`), and that you have write permissions to the s3 bucket (ask Andy or Aaron).

Then use the command `s3_website push`

# Develop

Hydra was built with [Jekyll](http://jekyllrb.com/) version 3.3.1, but should support newer versions as well.


Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

## Building Docs
Clone https://github.com/databricks/mlflow and follow the
[instructions for building docs](https://github.com/databricks/mlflow/blob/master/CONTRIBUTING.rst).

Copy over the html docs to the docs/latest and docs/`VERSION_NUM` directories.

Then redeploy the site.


# Jekyll Theme Attribution

This site was built on the MIT licensed Jekyll Hydra theme

Hydra was made by [CloudCannon](http://cloudcannon.com/), the Cloud CMS for Jekyll.

