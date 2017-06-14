# Shippy

## Why

We want a common tool to access our delivery infrastructure and development environments.

## What

A simple Python script, `ship.py`, will allow us to log into our platform tools ([OpenShift](openshift.md), [HashiCorp Vault](secrets.md)).

It will help us automate the cloning from [Starter Kit](../development/starter-kits.md) templates, by creating the GitHub repo, granting access to your squad, deploying it in OpenShift, connecting the webhook, and kicking off your delivery pipeline.

## How

Shippy core values:

### Safety

- Ensure our customer experience is great
- Automate operational compliance: test, content, API, delivery, design, arch, analytics, TDIM, release mgmt
- Tests: unit, integration, e2e, (opt: contract, device)
- Code Standards: follows reference architecture
- Practices: e.g. TDD, CI/CD, etc.
- Tools: Slack, Jira, GitHub, OpenShift, Jenkins, Kibana, NewRelic, PagerDuty, Swagger, Elasticache, multi-az RDS, (Hashi+Ansible) Vault

### Security

- Increase code quality / standards
- Keeping the baddies out of things
- Keeping us out of the news
- Automated testing during build
- Continuous testing after build

### Speed

- Applications are performant
- Outcome teams are empowered to be data-driven
- Outcome teams are able to get ideas out to customers quickly
- Use starter kit templates to give teams quick, safe, boilerplate projects
- Build pipeline executes in the shortest amount of time possible
- Incidents can be responded to quickly and efficiently

## Who

@delivery

## References

- [ship.py](https://github.com/telusdigital/ship.py)