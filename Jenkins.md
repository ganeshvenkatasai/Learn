
# Jenkins Cheat Sheet

## Basics

- Jenkins: An open-source automation server used for building, testing, and deploying applications.
- CI/CD: Jenkins automates Continuous Integration and Continuous Delivery workflows.
- Pipeline: A series of steps that Jenkins runs to build and deliver software.

## Installation & Setup

- Install Jenkins: Available via native packages, Docker, or WAR file.
- Start Jenkins: Usually runs on `http://localhost:8080` after setup.
- Initial Admin Password: Found in Jenkins home directory (`secrets/initialAdminPassword`).

## Jobs & Builds

- Freestyle Project: Simple job for building/testing code with basic configuration.
- Pipeline Job: Defines build process in code using `Jenkinsfile`.
- Build Triggers: Automatically start jobs on events (e.g., SCM change, schedule).
- Parameters: Input values passed to Jenkins jobs.

## Jenkinsfile

- Jenkinsfile: A text file that defines the pipeline as code.
- Declarative Pipeline: Simpler syntax using `pipeline {}` block.
- Scripted Pipeline: More flexible, uses Groovy script blocks.

## Pipeline Stages & Steps

- stage: A major phase in the pipeline (e.g., Build, Test, Deploy).
- steps: Actions inside a stage (e.g., `sh`, `echo`, `checkout`).

## Plugins

- Plugins: Extend Jenkins functionality (e.g., Git, Docker, Slack).
- Manage Plugins: Found under "Manage Jenkins" → "Manage Plugins".

## Source Code Management

- Git Integration: Jenkins can pull code from GitHub, GitLab, Bitbucket, etc.
- Webhooks: Trigger Jenkins jobs automatically on code push.

## Build Tools

- Maven: Java build tool, supported via plugin.
- Gradle: Another Java build tool, also plugin-supported.
- npm: For Node.js projects, can run via `sh 'npm install'` etc.

## Notifications

- Email Notifications: Send build result emails via plugin.
- Slack Notifications: Use Slack plugin to send build alerts to channels.

## Distributed Builds

- Master-Agent: Jenkins can distribute builds across multiple agents.
- Node: A machine configured to run Jenkins jobs.

## Security

- Users & Roles: Jenkins supports user authentication and role-based access.
- Credentials: Store sensitive info like passwords or tokens securely.

## Best Practices

- Use Pipeline as Code: Keep Jenkinsfile in source control.
- Use Agents: Distribute builds to avoid overloading master.
- Backup Jenkins: Regularly backup Jenkins home directory.
- Monitor Builds: Use Blue Ocean or build history to track status.

## Misc

- Blue Ocean: A modern UI for Jenkins pipeline visualization.
- Restart Jenkins: Can be done via `Manage Jenkins` or terminal.
