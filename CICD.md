# CI/CD

Basics : https://docs.gitlab.com/ee/ci/introduction/

We currently use [GithubActions](https://github.com/features/actions) to run all our test and deployment pipelines.

All projects should have Github Actions defined which do the following:

- Lint (Mandatory on new projects)
- Compile/Typecheck (Based on language)
- Test (At least the basic functionality works)
- Deploy (When merged to master/main)

Developers should not be deploying code to production. All changes/deployments to production environment should be done via the pipeline with approvals from the appropriate division lead. 

# Testing

Write basic tests which ensure your project will run properly if the tests pass.
This is integral to the CI/CD pipeline as we will be notified if something breaks before pushed to production.

Do not write too many tests just for the sake of it, as a startup, our requirements will be dynamic so a lot of tests will make progress slow.

Make use of Snapshot Tests where possible, makes writing tests easy.

# Testing Setup

The pypi link below provides code examples for how to set up snapshot testing; 

https://pypi.org/project/pytest-snapshot/




