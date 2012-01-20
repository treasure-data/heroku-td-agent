# Running td-agent on Heroku

This repository contains whole stack to run td-agent on Heroku platform. Please follow these steps.

## Clone Repository

  $ git clone git://github.com/treasure-data/heroku-td-agent.git

## Heroku

  $ heroku create --stack cedar
  $ git push heroku master

## Set Your API Key

  $ vi td-agent.conf

## Test

  $ curl "http://td-agent-on-heroku.herokuapp.com/debug.test?json=%7B%22json%22%3A%22message%22%7D"
  $ curl "http://td-agent-on-heroku.herokuapp.com/td.sample_db.sample_table?json=%7B%22json%22%3A%22message%22%7D"
