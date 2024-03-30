# CI/CD

- [CICD Labs](./devops-tools/CICD100.md)

## Deployment Strategies

### In-Place Deployment

Pros:

Simplicity: Straightforward to implement and understand, requiring minimal infrastructure changes.
Cost-effective: Does not require additional resources for parallel environments.
Familiarity: Commonly used, making it well-understood by many teams.
Cons:

Downtime: Likely to incur some downtime during deployment, affecting availability.
Riskier: Limited scope for testing in production-like environments, increasing the risk of deployment issues.
Rollback complexity: Rolling back a deployment can be complex and time-consuming.

### Blue/Green Deployment

Pros:

Zero downtime: Allows for live environment swapping, ensuring no service disruption.
Instant rollback: Easy and quick to revert to the previous version if issues arise.
Testing in production: Facilitates final testing in a production-like environment before going live.
Cons:

Cost: Requires double the environment resources, increasing infrastructure costs.
Complexity: More complex setup and management compared to in-place deployments.
Synchronization: Requires careful synchronization of databases and shared resources during the switch.

### Canary Releases

Pros:

Risk mitigation: Gradual rollout reduces the impact of errors on the entire user base.
Real user feedback: Enables gathering real-world usage feedback and performance metrics.
Scalable: Adjust the user percentage based on feedback and performance data.
Cons:

Management overhead: More complex to manage different versions among users.
Metric analysis: Requires sophisticated monitoring and analysis tools to measure impact accurately.
Rollout duration: Can take longer to fully deploy a feature or fix to all users.

### A/B Testing Deployment

Pros:

Data-driven decisions: Direct comparison of different versions to make informed decisions based on user interaction.
User-centric: Focuses on improving user experience and engagement.
Incremental improvement: Allows for continuous improvement of features based on user feedback.
Cons:

Complexity: Requires infrastructure to segment users and serve different versions.
Analysis resources: Needs significant resources for data collection, monitoring, and analysis.
Scope limitation: Typically limited to user-facing features, not suitable for backend changes.

### Automated Testing Integration

#### Pros

Quality assurance: Ensures code changes meet quality standards before deployment.
Early bug detection: Identifies and addresses issues early in the development cycle.
Confidence: Increases confidence in the stability of the application with each release.

#### Cons

Setup time: Requires time and effort to set up comprehensive test suites initially.
Maintenance: Test suites need regular updates to stay relevant to the application's evolution.
False positives/negatives: Risk of tests not accurately reflecting real-world usage or issues.

### Infrastructure as Code (IaC) for CI/CD Setup

#### Pros

- Consistency: Ensures infrastructure provisioning consistency and reduces manual errors.
- Speed: Accelerates the setup and scaling of environments.
- Version control: Infrastructure changes can be versioned and tracked like application code.

#### Cons

Learning curve: Requires understanding IaC syntax and best practices.
Initial setup: Takes time to define and test infrastructure code initially.
Complexity: Managing and organizing IaC for large-scale environments can be complex.

## Tools

### GitHub

##### Repo Tips

https://github.com/joelparkerhenderson/github-special-files-and-paths

##### Games

https://github.com/joshzcold/Cold-Family-Feud

##### Actions

[GitHub Action for pylint - GitHub Marketplace](https://github.com/marketplace/actions/github-action-for-pylint)

[Automating Dependabot with GitHub Actions - GitHub Docs](https://docs.github.com/en/code-security/dependabot/working-with-dependabot/automating-dependabot-with-github-actions)
