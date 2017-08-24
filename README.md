
# Redmine 3.4 on Heroku

<img src="https://cloud.githubusercontent.com/assets/296432/3865668/0fbd67c8-1fa3-11e4-9d4e-b33353725c60.png" width="75"/>

[Redmine] is a flexible project management web application. Written using the Ruby on Rails framework.

More details can be found in the doc directory or on the [official website](http://www.redmine.org).

## How to deploy [Redmine] on [Heroku]

1. Make sure you have the [Heroku Toolbelt] installed.
2. Click this button and follow the instructions: <BR/> [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)
3. After you have an instance running on Heroku, run these commands in your terminal.

```
$ heroku git:clone -a <YOUR-APP-NAME>
$ cd <YOUR-APP-NAME>
$ heroku run rake redmine:load_default_data
$ heroku run rake redmine:plugins:migrate RAILS_ENV=production
```

You can now log into your Redmine installation using the initial user account (username: `admin`,  password: `admin`).

## License

Like [Redmine], this is open source and released under the terms of the [GNU General Public License v2 (GPL)](http://www.gnu.org/licenses/old-licenses/gpl-2.0.html)

[Redmine]: http://www.redmine.org
[Heroku]: https://www.heroku.com
[Heroku Toolbelt]: https://toolbelt.heroku.com
