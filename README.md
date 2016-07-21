## GOV.UK CI Scripts

This repo contains scripts to run the tests for GOV.UK projects on Jenkins.

## Usage in Rails applications

In `jenkins.sh`:

```sh
#!/bin/bash

export REPO_NAME=${REPO_NAME:-"alphagov/my-rails-application"}
curl https://raw.githubusercontent.com/alphagov/govuk-ci-scripts/master/rails-app.sh | bash
```

## Usage in Gems

In `jenkins.sh`:

```sh
#!/bin/bash

export REPO_NAME=${REPO_NAME:-"alphagov/my_gem"}
curl https://raw.githubusercontent.com/alphagov/govuk-ci-scripts/master/gem.sh | bash
```

## Usage in non-Rails projects

TODO.

## Adding schema tests


In `jenkins-schema.sh`:

```sh
#!/bin/bash

export REPO_NAME="alphagov/govuk-content-schemas"
export CONTEXT_MESSAGE="Verify my_gem against content schemas"

exec ./jenkins.sh
```
