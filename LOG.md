1. Initialize the project based on https://github.com/heroku/php-getting-started

2. Replace `/web/index.php` file with the `index.php` provided in the exercise

3. Follow the `README.md` provided in the exercise to complete steps 1-7

4. Deploy the project to check (step 10)

5. Validate environment variables have been added successfully

6. Encounter issue when trying to follow steps 11-13. 
   By examining the logs from Heroku, `$_POST['body']` does not seem to work in this case.
   After some research, replacing `$_POST['body']` with `file_get_contents('php://input')` to check.
   
7. Fix bug `Trying to get property 'type' of non-object in /app/web/index.php on line 13`

8. Fix bug `Array to string conversion in /app/web/index.php on line 25`

9. Add `default` block for `switch` statement

10. After triggering `user_change` event, some logs can be found in Heroku with very general info. Nothing comes up in the app. Adding more logs to check.

11. Fix the event name from `status_change` to `user_change`

12. Found a bug `Undefined property: stdClass::$real_name_normalized in /app/web/index.php on line 33`. Add a debug log to check the structure of the `event->user`.

13. Fix the bug in #12 by adding the missing layer `profile` between `user` and `real_name_normalized`

14. Add a debug log to validate `$payload` for `postMessage` function
