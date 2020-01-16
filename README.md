# standup
Keep track of tasks per day for standup purposes

The script generates a daily markdown file where you keep tracks of notes and tasks. It also generates a report and sents it to an email address.

## Installation

    pip install --user --requirement requirements.txt

## Usage

Decide where you want to store your data. I use dropbox and will use $HOME/Dropbox/standup

### Generate daily markdown file and open editor with newly create file

    standup open -l $HOME/Dropbox/standup

You can setup your system to run this command when you log in, so no work required from your side!

### Daily report

The report detects the previous day's file, as well as today's file, converts both to html and sends it to an email.

    standup report -l $HOME/Dropbox/standup -s <SMTP Server> -p <SMTP Server Port> -u <Username> -f <From Address> -t <To Address>

I have setup a cron job to run this command 15 before I go to standup
