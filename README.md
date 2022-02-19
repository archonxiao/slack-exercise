# slack-exercise

The app makes use of Slack's Events API. It listens to the `user_change` event for a user changing status, and then posts a message containing their custom status to the #statuses channel in their Slack workspace.

This app is build on top of a starter heroku project:
https://devcenter.heroku.com/articles/getting-started-with-php

The `index.php` file is located at `/web/index.php`

The `LOG.md` keeps all the work logs