# Jekyll Rackup Build Pack 

Forked from (thanks Mark!):

  https://github.com/markpundsack/heroku-buildpack-jekyll

As I wanted to added a permanent redirect from www to the canonical domain. 

Check out the following gist for a sample `config.ru` file.

  https://gist.github.com/1957045

The Jekyll Build Pack will look for a file named `_config.yml` in the app root and
run Jekyll to create and serve the site.

## Usage

Add this language pack to your `BUILDPACK_URL`.

    heroku config:add BUILDPACK_URL="http://github.com/snapper/heroku-buildpack-jekyll-rackup.git"
    
Or, with a recent version of the heroku gem, set it at creation time:

    heroku create --stack cedar --buildpack http://github.com/snapper/heroku-buildpack-jekyll-rackup.git
