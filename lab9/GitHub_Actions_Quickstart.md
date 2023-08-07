# Github Actions

**DevOps Toolchain Category:** Version control, CI-CD

## Setting up the First GitHub Actions Pipeline:

**Overview:** The process was straightforward. The steps to set up this pipeline included:

- Initializing a '.github/workflow' directory from the project source.
- Within this directory, I created a 'github-actions.yml' file.
- Actions to be executed were then copied and pasted into the 'github-actions.yml' file.
- Subsequent to these changes, I committed them to the branch.

**Key Insight:** Every time a commit is pushed to the branch containing the workflow-actions, the specified actions in the YAML file are triggered.

## Manual Triggering and System Information Gathering:

### Configuring a Manual Trigger:

To incorporate a manual trigger to my workflow, I:

- Edited the workflow file to introduce a new trigger (`workflow_dispatch` event).
- Integrated this event within the "On" key section.
- Committed and saved these modifications.

**Observation:** A "Run Workflow" button appeared in the GitHub repository's workflow list corresponding to the edited workflow. To initiate it, I clicked the "Run Workflow" button without inputting any parameters.

**Crucial Note:** For GitHub Actions to detect the workflow dispatch, merging the branch with the main branch was necessary, as highlighted in the GitHub Actions documentation.

### System Information Extraction:

#### Process:

For detailed system analysis, I amended my workflow to incorporate two actions: "Get hardware specifications" and "Get OS details." System commands were leveraged to extract the necessary data.

##### Hardware Details:

```sh
- name: Get hardware specifications
    run: |
        echo "CPU: $(uname -m)"
        echo "CPU cores: $(nproc)"
        echo "Memory: $(free -m | awk '/^Mem:/ {print $2}')"
        echo "Disk space: $(df -h | awk '/^Filesystem/ {print $2}')"
```

##### Operating System Information:

```sh
- name: Get OS details
    run: |
        echo "OS: $(cat /etc/os-release | grep ^NAME | cut -d'=' -f2)"
        echo "OS version: $(cat /etc/os-release | grep ^VERSION_ID | cut -d'=' -f2)"
```
