Gitlab Runners sometimes get stuck or have system failures. To save developers the hassle of having to restart them manually we want this to happen automaticly. 

This repo contains a file, that can be included in your `.gitlab-ci.yml` to get this behaviour imported.

## Setup Instructions
At the very top of your .gitlab-ci.yml either add or expand the `include:` section so it looks similar to this:  
```yaml
include:
  - remote: https://raw.githubusercontent.com/ambient-innovation/gitlab-retry-runners/main/gitlab-retry-runners.yaml
  # There might be more includes here, usually starting with template like the following:
  # - template: 'Workflows/Branch-Pipelines.gitlab-ci.yml'
```