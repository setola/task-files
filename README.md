# task-files
A collection of taskfiles for everyday use

You can include these task using the [remote taskfile](https://taskfile.dev/experiments/remote-taskfiles/) feature

```yaml
version: '3'
vars:
  TASK_FILES_REPO_RAW: https://github.com/setola/task-files/raw/refs/heads/main/
includes:
  docker: "{{ .TASK_FILES_REPO_RAW }}/docker"
  dc: "{{ .TASK_FILES_REPO_RAW }}/docker-compose"
  os: "{{ .TASK_FILES_REPO_RAW }}/os"
  ssl: "{{ .TASK_FILES_REPO_RAW }}/ssl"
```

or clone the repo and include taskfiles locally; remember to adjust `INSTALL_DIR` to your local cloned repo directory:

```yaml
version: '3'
vars:
  INSTALL_DIR: ~/taskfiles
includes:
  docker: "{{ .INSTALL_DIR }}/docker"
  dc: "{{ .INSTALL_DIR }}/docker-compose"
  os: "{{ .INSTALL_DIR }}/os"
  ssl: "{{ .INSTALL_DIR }}/ssl"
```