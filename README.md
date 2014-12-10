# Treasure Agent on Heroku

This repository contains everything to run Treasure Agent on Heroku. [HTTP plugin](http://docs.fluentd.org/articles/in_http) is used to receive the streaming logs. For further information, please look at [this documentation](http://docs.treasuredata.com/articles/heroku-rest).

## Setup

There is no step 1. Just click on the Heroku Deploy button here.

<a href="https://heroku.com/deploy?template=https://github.com/treasure-data/heroku-td-agent"><img src="https://www.herokucdn.com/deploy/button.png"/></a>

By default, a new Treasure Data account is created. If you already have an account with a [Treasure Data API key](http://docs.treasuredata.com/articles/get-apikey), fill out the "TREASURE\_DATA\_API\_KEY\_OVERRIDE" field.

<img src="https://raw.githubusercontent.com/treasure-data/heroku-td-agent/master/heroku-td-agent-screenshot.png"/>


## Testing

    # debug
    $ curl "http://<YOUR_APP_NAME>.herokuapp.com/debug.test?json=%7B%22json%22%3A%22message%22%7D"
    
    # import
    $ curl "http://<YOUR_APP_NAME>.herokuapp.com/td.sample_db.sample_table?json=%7B%22json%22%3A%22message%22%7D"
