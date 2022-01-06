# Cloud Formation for DMS

## Source

Following this tutorial:

- <https://aws.amazon.com/blogs/database/automating-database-migration-and-refreshing-activities-with-aws-dms/>

- <https://docs.aws.amazon.com/lambda/latest/dg/services-cloudwatchevents-expressions.html>

- (?) <https://aws.amazon.com/blogs/database/automating-aws-dms-migration-tasks/>

## How to create new template

### Way 1

Duplicate a new file from `template.yml` then replace these text:

- dataprocess-eventenable-lambda-role
- dataprocess-eventenable-lambda
- dms-task-starter-lambda-role
- dms-task-starter-lambda
- dms-task-statechange-topic
- dmstask-scheduler-eventrule
- dmstasksubscription

- UseExistingReplicationTask: no -> yes
- ExistingDmsReplicationTaskName: value name (eg: move-data-from-agent-feedback)

### Way 2

Duplicate new file from a file that are running, eg: `crawler.yml`. Then replace all `crawler` to `your_text`

Note: `your_text` is the name of dms task
