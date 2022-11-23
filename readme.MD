Hi here we are completing tutorials on CI/CD task.
The CI/CD tool built and used by GitHub—Actions—allows you to build, test and deploy your code straight from GitHub, taking care of all the automation to make it happen smoothly. The possibilities are endless!
<b>Covering some basic information about github actions if already know you can skip to implemenation guide.</b> <a href="#Sec-1">Implementation</a><br/>



# What is Github Actions?
First, we need to establish the distinction between "GitHub Actions" and an "Action". The former is the product's name and the latter is custom code that you can include in a workflow job as a step to accomplish a task.
GitHub Actions is the continuous integration and continuous delivery tool built and used by GitHub. It allows you to build, test and deploy your code straight from GitHub, taking care of all the automation that enables this to happen smoothly without any third-party CI/CD tools. The possibilities you can build and automated SMS service provider to alert you when an urgent issue is created in your repo. Or it can turn on your coffee machine when you create a new pull request.

## What are the components of GitHub Actions?
- Events
- Workflow
- Job
- Step
- Runner

<i>Let's break down this diagram, starting from the left and going right:<br></i>
![image](https://user-images.githubusercontent.com/90677747/203483631-ad96cf6c-818d-44cc-9aa2-ea914a378f2c.png)

<b>Event</b> : This is the event that triggers the action. It represents an activity in the repository that will trigger a workflow run.<br>
- `Push` : Triggers when a user pushes into a branch
- `Pull_request` : Triggers when a pull_request is received on the repository. Can be specified to match only certain types of pull_requests like opened etc.
- `Fork` : Triggers whenever the repository is forked.
- `Issues` : Triggers when an issue is changed. Can be specified to match certain types like opened, closed, etc.
- `Release` : Triggers when a release on the repository is created.
<br>There are many events that you can listen for, a full list can be found on the - [GitHub docs](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows).


<b>Workflow</b> : A workflow is an automated process composed of a series of jobs that gets executed when it’s triggered by an event.
Workflows are defined in YAML files and are stored in a `.github/workflows` directory at the root of the repository. A repository can also have multiple workflows.


<b>Job</b> : Jobs are set by using the jobs keyword in the workflow configuration.
Jobs can be configured to run with many useful settings. You can create needed Docker containers and much more to run in the Jobs, or even change the operating system that it runs on. Jobs can contain many steps. A workflow can have multiple jobs that run in parallel.

<b>Step</b> :  A step is an actual action to perform .It is a name for a certain command or series of commands. Steps reside inside Jobs and are set by using the `steps` keyword. 

<b>Runner</b> : Runners are processes on a server that run the workflow when it’s triggered. Each runner is responsible for executing a given job.
Runners are hosted in the cloud but they can also be [self-hosted](https://docs.github.com/en/actions/hosting-your-own-runners) in custom cloud environments.







<hr>
<h2 id="Sec-1">Implementations Started</h2>
Copy implement form https://betterprogramming.pub/github-actions-in-action-3b10083cc700 
How he created what are events on is use for event creat that here.
<p>
```
Event listeners are configured using the `on` keyword inside our GitHub Actions configuration. You can use multiple event listeners
```
</p>
    
