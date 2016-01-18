# moo

An express wrapper for cowsay, so you can moo like you mean it in Slack.

## Usage

```bash
/moo yoyoyo
```

Gives:

```bash
 ________
< yoyoyo >
 --------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

## Installation

### Local

Install [nodemon](http://nodemon.io) to make your life easier!

Then clone this repo from GitHub and install the Node.js dependencies.

```bash
git clone git@github.com:mikefrancis/moo.git
cd moo
echo "SLACK_TOKEN=testSlackToken" >> .env
npm install
```

Once installed, run `nodemon` to start the express server and watch for changes.

To test, send a `POST` request to the index of the server containing the following `body`:

```json
{
 "token": "testSlackToken",
 "text": "yoyoyo"
}
```

### Live

Click the button below:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

And make a note on your app's URL.

Then head to Slack and create a custom Slash Command, paste in your app's URL to the Integration URL field, and make a note of your `token`.

Head back to your Heroku app's Settings > Config Variables and create a new `SLACK_TOKEN` with the `token` value from above.
