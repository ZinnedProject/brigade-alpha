Brigade Alpha
=============

We’ve started work on the [new Brigade website](http://brigade-alpha.codeforamerica.org). It is still very much a work in progress, yet we share early and often around here. The site at this repository is intended to eventually replace the [CfA Brigade site](http://brigade.codeforamerica.org).

We have a few main goals with this early prototype:

1. Clearly explain what the Brigade is.
2. Make it easy to find a local Brigade. The links on the map bring you directly to the Brigade's remote site.
3. An invitation to join that local Brigade. This join form uses the existing sign up logic from the main site that connects you to the local captain.

Install
-------

Mostly, everything here is plain HTML. The app is run under Python Flask, which we will soon start using to host an actual database-driven API. But not yet.

The scheduled update task should be run every 10 minutes. Set up Heroku
[scheduled tasks](https://devcenter.heroku.com/articles/scheduler) with
two commands:

    heroku addons:add scheduler:standard
    heroku addons:open scheduler

The command to run is:

    python update-data.py

Heroku will access [brigade information](https://docs.google.com/a/codeforamerica.org/spreadsheet/ccc?key=0ArHmv-6U1drqdGNCLWV5Q0d5YmllUzE5WGlUY3hhT2c) from Google Docs without authentication. A `GITHUB_TOKEN` environment variable can be used to help circumvent Github API throttling; get one under your [settings/applications](https://github.com/settings/applications).

Contact
-------

* Andrew Hyder ([ondrae](https://github.com/ondrae))
* Frances Berriman ([phae](https://github.com/phae))
* Michal Migurski ([migurski](https://github.com/migurski))
