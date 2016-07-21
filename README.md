## GOV.UK CI Scripts

This repo contains scripts to run the tests for GOV.UK projects on Jenkins.

## Set up

In `jenkins.sh`:

```sh
#!/bin/bash

export REPO_NAME=${REPO_NAME:-"alphagov/content-tagger"}
curl https://raw.githubusercontent.com/alphagov/govuk-ci-scripts/master/rails-app.sh | bash
```

In `jenkins-schema.sh`:

```sh
#!/bin/bash

export REPO_NAME="alphagov/govuk-content-schemas"
export CONTEXT_MESSAGE="Verify content-tagger against content schemas"

exec ./jenkins.sh
```
