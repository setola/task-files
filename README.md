# task-files
A collection of taskfiles for everyday use

You can include using the [remote taskfile](https://taskfile.dev/experiments/remote-taskfiles/) feature

```yaml
version: '3'
vars:
  TASK_FILES_REPO_RAW: https://github.com/setola/task-files/raw/refs/heads/main/
includes:
  os: "{{ .TASK_FILES_REPO_RAW }}/os/Taskfile.yml"
  docker: "{{ .TASK_FILES_REPO_RAW }}/docker/Taskfile.yml"
  dc: "{{ .TASK_FILES_REPO_RAW }}/docker-compose/Taskfile.yml"
```

or clone the repo and include taskfiles locally:

```yaml
version: '3'
vars:
  INSTALL_DIR: ~/taskfiles
includes:
  os: "{{ .INSTALL_DIR }}/os"
  docker: "{{ .INSTALL_DIR }}/docker"
  dc: "{{ .INSTALL_DIR }}/docker-compose"
```