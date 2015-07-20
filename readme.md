Redmine Issue
=============

Command line application that allows to manage issues in redmine easily. Optimized for idfly.ru custom workflow.


Installation
------------

gem install redmine-issue
redmine-issue set-config secret [YOUR API KEY AT http://HOST/my/account]
redmine-issue set-config address "http://HOST"


Commands
--------


### list

  List issues; arguments is API get params: http://www.redmine.org/projects/redmine/wiki/Rest_Issues;
  Example: --project-id 10 --status-id closed; default arguments: --assigned-to-id me --status-id open
    --sort "priority:desc,project"


### description [id]

Get issue description and comments.


### reply [id] -m message

Reply to issue; adds comment, sets status "Feedback" and returns issue to responsible user


### start id

Starts issue specified by id; starts tracking current issue and spent time and set issue status "In progress"


### pause

Pause current issue; save spent time to issue and untrack current issue.


### cancel

Cancel current issue; untrack current issue without time saving.


### status

Get current issue id and spent time.


### complete [id]

Complete issue; set status "Completed" to issue and returns issue to responsible user; if completes current -
save spent time.


### close [id]

Same as complete but set status "Closed"; you have to have permission to close issues to tun this command.


### config key

Displays config value.


### set-config key value

Sets config value.


