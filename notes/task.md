# TASK

## 1. Create task config `tasks.json` (one time)

`Terminal > Configure Tasks > Create tasks.json file from template`. Select one from list templates. E.g., select `Others` to run external command.

This creates `.vscode/tasks.json` at proj root with content:

```json
{
  // See https://go.microsoft.com/fwlink/?LinkId=733558
  // for the documentation about the tasks.json format
  "version": "2.0.0",
  "tasks": [
    {
      "label": "echo",
      "type": "shell",
      "command": "echo Hello"
    }
  ]
}
```

## 2. Change `tasks.json` as needed

E.g., create build task to compile `md` file to `html`.

```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Compile Markdown",
      "type": "shell",
      "command": "markdown-it sample.md -o sample.html",
      "group": "build"
    }
  ]
}
```

## 3. Run task

`Terminal > Run Task` or `Run Build Task` (`Shift + Command + B`) if task configured to be build task.

### 3a. Default build task

To configure default build task: `Terminal > Configure Default Build Task`

This changes task's `group` field:

```json
"group": {
  "kind": "build",
  "isDefault": true
}
```
