# td-agent on Heroku

This repository contains whole stack to run td-agent on Heroku platform. [HTTP plugin](http://docs.fluentd.org/articles/in_http) is used to receive the streaming logs. For further information, please look at [this documentation](http://docs.treasuredata.com/articles/heroku-rest).

### 1) Clone this repository

    $ git clone git://github.com/treasure-data/heroku-td-agent.git
    
### 2) Set your API key

Please access to [here](https://console.treasuredata.com/users/current). At the right most column, you can retrieve the API key.

    $ vi td-agent.conf
    $ git commit -a -m 'update apikey'

### 3) Heroku

    $ heroku create --stack cedar
    $ git push heroku master

### 4) Test

    # debug
    $ curl "http://td-agent-on-heroku.herokuapp.com/debug.test?json=%7B%22json%22%3A%22message%22%7D"
    
    # import
    $ curl "http://td-agent-on-heroku.herokuapp.com/td.sample_db.sample_table?json=%7B%22json%22%3A%22message%22%7D"
