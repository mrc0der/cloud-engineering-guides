# CI/CD Labs

## Task 1: Implement In-Place Deployment

**Title:** Implement In-Place Deployment for a Web Application

**Goal:** Learn to perform an in-place update, where the application is updated on the existing infrastructure without changing the environment.

**Description:**

- Use a simple web application to implement an in-place deployment strategy.
- Automate the deployment process using a CI/CD tool (e.g., Jenkins, GitLab CI).

**Acceptance Criteria:**

- Successful update of the application on the same infrastructure without downtime during off-peak hours.
- Documentation of rollback strategy in case of deployment failure.

## Task 2: Blue/Green Deployment

**Title:** Execute a Blue/Green Deployment Strategy

**Goal:** Understand and implement blue/green deployments to reduce downtime and risk by running two identical environments.

**Description:** Set up two identical environments: Blue (current production) and Green (new version).
Automate the switch from Blue to Green environment using a CI/CD pipeline once the new version is fully tested and ready.

**Acceptance Criteria:**

- Zero downtime during the switch from Blue to Green environment.
- Validation tests confirm that the Green environment is functioning as expected before the switch.
- Documentation of the process, including how to roll back to the Blue environment if issues arise.

## Task 3: Canary Releases

**Title:** Implement Canary Releases

**Goal:** Learn to gradually roll out changes to a small subset of users before a full rollout, to minimize risk.

**Description:** Modify the CI/CD pipeline to support releasing updates to a small percentage of the total user base.
Increase the rollout percentage based on monitoring and feedback.

**Acceptance Criteria:**

- Successful deployment of the new version to a limited user base without affecting the entire application.
- Monitoring in place to capture feedback and performance of the new release.
- Criteria defined for increasing the rollout percentage and for rollback if necessary.

## Task 4: A/B Testing Deployment

**Title:** Set Up A/B Testing Deployment

**Goal:** Implement A/B testing to compare two versions of an application and analyze user engagement and performance.

**Description:** Create two versions of a feature within the application. Use a CI/CD tool to deploy both versions to a portion of the user base. Collect and analyze metrics to determine the better-performing version.

**Acceptance Criteria:**

- Both versions of the feature are deployed simultaneously without affecting the overall application performance.
- Data collection and analysis setup to evaluate the performance of both versions.
- Documentation on decision-making based on collected data and subsequent actions.

## Task 5: Automated Testing Integration

**Title:** Integrate Automated Testing in CI/CD Pipeline

**Goal:** Incorporate various automated testing stages (unit, integration, and end-to-end tests) into the CI/CD pipeline to ensure code quality and reliability.

**Description:** Define and implement automated tests for a web application. Integrate these tests into the CI/CD pipeline, ensuring they run at appropriate stages.

**Acceptance Criteria:**

- Successful integration of automated tests into the CI/CD pipeline.
- Tests are automatically triggered at each code commit and prior to deployments.
- Test results are documented, and failures halt the deployment process until resolved.

## Task 6: Infrastructure as Code (IaC) for CI/CD Setup

**Title:** Automate CI/CD Infrastructure Setup using IaC

**Goal:** Use Infrastructure as Code to automate the setup and teardown of CI/CD pipeline infrastructure.

**Description:** Utilize an IaC tool (e.g., Terraform, CloudFormation) to define the infrastructure required for a CI/CD pipeline.
Automate the provisioning and de-provisioning of resources for CI/CD workflows.

**Acceptance Criteria:**

- Infrastructure for the CI/CD pipeline is provisioned automatically using IaC scripts.
- Documentation on how to use the IaC scripts to recreate the infrastructure.
- Ensure the teardown process cleans up resources to avoid unnecessary costs.
