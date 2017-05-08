# Git Practices

## Why

- As a tool Git combined with GitHub provides countless styles of development and project management with many options for configuration such as:
    - Trunk based development (w/feature flagging)
    - GitFlow (branches/features)
    - Pull Requests (core contributers / open source)
    - Git hooks (pre-commit hooks, pre-push hooks, etc)

- Too many configurations are problematic:
    - Increase time required to onboard new developers
    - Increases friction in developers contributing to other team projects
    - Increases time to development on new projects as teams reinvent configuration

- The goal of this document is to:
    - define some broad expectations that each project should meet
    - define some agreed upon practices for hooks and their roles
    - define some broad practices regarding contribution models
    
## How

### GitHub Readme
Every project should have a readme that clearly expresses the following:
- The purpose, scope and goals of the project
- The author / current owners
- Clear up to date instructions on:
    - Setup and installation
    - Running your app (if applicable)
    - Basic usage (API, Endpoints, etc)
    - List of bundled scripts, such as:
        - How to run tests
        - How to run linting
        - etc

### Git Hooks
 Git hooks should not exist as a replacement for good practices, education or mentorship. Teams are encouraged to focus on small feature branches, with proper PR process (utilizing CI tools as a sanity check and auditing step), and a low friction contribution model as opposed to over reliance on git hooks and custom steps.
 
 Git hooks are acceptable if a team collectively feels they will provide a benefit, but should if used should not result in a heavy burden, or time cost for each commit. In this way `pre-push` hooks may be more suitable in many cases where running an entire test suite, or other tools may start to feel burdensome.


### Contribution Model

There has been a constant swing between Trunk Based Development and Branch style development for many years. Reasonably so, both are seen to have advantages and disadvantages. 
- Small branches with Pull Requests encourage a social open source model, a living form of documentation, and an easy way for external contributors to see and understand the contribution model
- Trunk Based development can assist in reducing defects and reduce day to day frictions for core team members. 

In this way teams are encourage to adopt a hybrid approach:
- Each project should have core owners that oversee the vision of the project, and can reject/approve Pull Requests and are responsible for supporting and communicating with interested contributors.
- Teams should be comfortable using small branches with PRs, and should practice this as a way of creating transparency in the code base and encouraging external contributors to participate
- Trunk based development is acceptable, but more as a philosophical approach to reducing internal day to day frictions for the core team, not as a mandate
 
## References

- [Readme.md Template][readme-template]
- [How to use Git Hooks][git-hook-guide]
- [Open Source Guides][open-source-guides]
- [Trunk Based Development - History][trunk-based-development]

[open-source-guides]: https://opensource.guide/ "Open Source Guides"
[git-hook-guide]: https://www.digitalocean.com/community/tutorials/how-to-use-git-hooks-to-automate-development-and-deployment-tasks "How to use Git Hooks"
[trunk-based-development]: https://trunkbaseddevelopment.com/game-changers/ "History of Trunk Based Development"
[readme-template]: https://gist.github.com/PurpleBooth/109311bb0361f32d87a2 "GitHub Readme Template"