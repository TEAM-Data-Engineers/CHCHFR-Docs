# CHCH-Fuel-Recommendator Project Git Workflow

## Overview

This project focuses on data engineering and involves the development of microservices for the frontend, backend, and mobile end. We will use PostgreSQL and MongoDB databases. GitHub issues and projects will be utilized for project management, and multiple repositories will be created under our organization.

## Git Repository Organization

The following repositories will be created under our organization:

- `Docs` - Repository for backend microservices code
- `data_engineering_petrol_pump` - Repository for extracting the basic dataset

## Branch Management

We will adopt the following branch management strategy:

- `main`: Contains the stable versions. It will be merged from the `production` branch, and then a tag version will be created.
- `production`: Branch for the production environment, merged from the `development` branch.
- `development`: Branch for integrating all features and fixes. Everyone should check out from this branch. All code submissions and merges should go through Pull Requests to ensure code review and testing.
- `feature`: Each developer should create their own feature branches based on their tasks/features from the `development` branch, named as `feature/<feature-name>`, for example, `feature/user-authentication`. After the feature is developed and tested, create a Pull Request and assign a code review member to merge the feature branch into the `development` branch.
- `hotfix`: Branch for emergency fixes in the production environment. It should be created from the `production` branch and merged back after fixing. It should also be merged into the `development` branch.

## Workflow Process

### Create Tasks and Issues

Use GitHub Issues to track tasks and issues. Each task should have a clear title and description, assigned personnel (if applicable), categories, and due dates (if applicable). Utilize Projects to organize and manage tasks to ensure timely tracking of progress.

### Create Feature Branches

Create a new feature branch from the development branch, named as `feature/<feature-name>`.

### Develop and Submit Code

Develop and test on the feature branch. Small feature changes should be completed in a single commit with clear commit messages. Once the feature is developed and tested, create a pull request to merge it into the development branch.

### Code Review and Merge

Submit a Pull Request (PR) to merge the feature branch into the development branch. At least one team member should perform a code review, and upon approval, merge the code into the development branch.

### Deploy to Production

When the code in the development branch is ready for release, create a release Pull Request to merge the code into the production branch. After testing and validation, deploy the production branch to the production environment.

### Release Stable Versions

Merge the production branch into the main branch and tag the version to maintain version consistency and stability.

### Emergency Fixes

If issues are found in the production environment, create a fix branch from the production branch and merge it back after fixing. It should also be merged into the development branch.

## Additional Notes

- Use meaningful commit messages for all submissions and merges to help team members understand the changes and purposes of each modification.
- All code changes should undergo appropriate testing to ensure no new issues are introduced or existing functionality is affected.
- Maintain code cleanliness and maintainability at all times to avoid unnecessary code redundancy and complexity.
- Regularly update the development branch with the latest changes from the main branch to avoid conflicts and ensure code consistency.
- Communicate with team members regularly to ensure everyone is on the same page and aware of the latest updates and changes.
- Utilize GitHub features such as Issues, Projects, and Pull Requests to streamline project management and collaboration.
