# CICD
## Jenkins
### Basics of Jenkins
Prior to creating Pipelines, you need to know a few basic pipeline-related terms. Let's take a look at them:

- Master - A machine where Jenkins is installed. It centrally stores all the configurations, loads plugins and renders the Jenkins UI.
- Agent - A machine which connects to the Jenkins Master and performs various operations as directed by the Jenkins Master.
- Node - A machine that can allocate an executor and run Jenkins Pipelines. Examples are Jenkins Masters and Agents.
- Step - A single task that tells Jenkins what to do at a given point in time. Examples include: executing a simple shell script and windows batch script.
- Stage - It is composed of logically distinct steps. Build, Test, Deploy are all examples of Stages. Stages are used for visualization of the Pipeline status/progress.


CI/CD workflow with the following set of stages:
- Build - In this stage, source code is compiled and built, and an artifact is generated.
- Test - In this stage, tests will be run in parallel on two different OS platforms, Linux and Windows.
- Deploy Staging - In this stage, the artifacts will be deployed to a staging environment (essentially a pre-production server). If everything is good, we will request for approval to deploy to production.
- Deploy Production - In this stage, artifacts will be deployed to the production environment.
