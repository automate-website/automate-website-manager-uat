# Manager User Acceptance Tests
This project contains manager application user acceptance tests written in web automation markup language.

Project scenarios can be executed using [WebRobotJS].

Refer to the [changelog] for recent notable changes and modifications.

## Project Structure

```
	/params
		<page name>-page.yaml
		data.yaml
		site.yaml
		params.yaml
	/tasks
		<task name>.yaml
	/actions
		<action name>.yaml
	/stories
		<story name>.yaml
```	

### Params
Contains both common site parameters like *baseUrl* and specific page parameters that are utilized in *tasks*, *actions* and *stories*. It also contains [data.yaml] that aggregates available user data.

All parameters are combined inside [params.yaml]

Params are fragments and can't be executed standalone without a context.

### Tasks
Contains small pieces of work that may be performed by the user like navigate to a page or ensure being at a certain page.

Params and tasks may be utilized in a certain task.

Tasks are fragments and can't be executed standalone without a context.

### Actions
Contains complex pieces of work that may be performed by the user, like the login process including navigation to the login page, typing credentials and pressing login button.

Params, tasks and actions may be utilized in a certain action.

Actions are fragments and can't be executed standalone without a context.

### Scenarios
Contains test scenarios that represent parts of the user's customer journey.

Scenarios may be executed standalone.

## Local Execution
Scenarios may be executed using [WebRobotJS] by running:

	`$ cd <runner path>`
	`$ node index.js --scenarioPath="<project path>"`

### Runner Path
The path to the [WebRobotJS];

### Project Path
The path to the manager user acceptance tests project.

[WebRobotJS]: https://github.com/automate-website/webrobotjs
[changelog]: CHANGELOG.md
[params.yaml]: params/params.yaml
[data.yaml]: params/data.yaml
