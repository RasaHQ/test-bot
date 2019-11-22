This is a bot used to test Rasa X releases

Integrated Version Control + [Roberto (@rasabot)](https://github.com/rasabot)  = <3

**Steps to set up for testing:**

1) run `git checkout tags/<tag_name> -b <branch_name>` to create a new branch off the release you want to test.

2) Make a change to the `rasa-x` repo, commit and push your changes, and then open a pull request

3) [Roberto (@rasabot)](https://github.com/rasabot) will automatically deploy an EE instance for that PR

4) Use `Integrated Version Control` to load this bot into that Rasa X instance

5) Test!

*WIP: Go to GCP and start `test-bot-action-server`, adjust the IP address of the action server in `endpoints.yml`, and run `rasa run actions`*
