# SCSDG - Smart Contract Secure Development Guidelines
Smart Contract Secure Development Guidelines (SCSDG) - high-level recommendations for developer teams that describe how to reduce risks related to smart contract (or system) security

## Preparation
Preparation processes defines the steps should be taken before the development starts

### Developer Security Education
- Developers should have basic knowledge about smart contracts security: best practices for the development, what vulnerabilities exist etc.
- It is highly recommended to check the developers security knowledge before project starts

### Compliance Management
- All legal and other compliance requirements should be analyzed prior the projects starts
- Third-party systems contract that will interact with the project can have legal and technical requirements, so they should be considered while requirements development

### Threat Assessment
- Threat assessment should be performed at the start of the projects
- All defined risks should be mitigated, transferred or accepted

## Documentation
Documentation processes defines what documentation should be developed within the project  

### Architecture Documentation
- High-level architecture description should be documented
- Documentation should specify what functionality of system is done via smart contracts, frontend and other parts of application
- Create a knowledgebase with integration notes: third-party integration requirements, developer manuals etc.

### Requirements Documentation
- All requirements for the system (including smart contracts, frontend etc.) should be documented. All system's desired functionality should be covered by requirements
- The timeline of the development project should be predefined with deadlines for all stages (for example, develop code till xx.xx, test till yy.yy, do audits till zz.zz). It is highly recommended to agree on terms of the third-party audit in advance

### Deployment Documentation
- Deploy script should be developed and tested. The tests results and how-to use it guide should be documented
- Deployment environment and tools should be predefined and documented (compiler type and version, tools/scripts for deployments etc.)

## Development
Development process security practices define how-to develop more secure code

### Integration management
- All integrations within the project (for example, with frontend) should be carefully done, tested and reviewed by security professional
- Code should be tested against third-party integrations, for instance, exchanges, other smart contracts

### Template management
- It is highly recommended to use templates audited by several security experts rather develop own code. All parts of code that can be developed via secure templates should use them, for example, OpenZeppelin template contracts for tokens
- All code developed using template should contain references to template origin and documentation

### Tools Management
- All frameworks, testing tools, etc. should be the same for all developers within the project
- Developers should use code linters for increasing code quality
- Developers should use static code analyzers while development - each release should be checked

## Security Operations
Security Operations define processes that should be implemented for managing the project securely

### Role Management
- All roles (privileged accounts) within the DApp should be defined. List of people with extra access should be documented.
- The roles within the system should be aligned with business requirements. The list privileged principle should be applied

### Issue/Bug Management
- Issues found by the audits should be internally reviewed and only applicable bugs should be fixed
- All tests should be re-performed after each smart contract code change
- It is highly recommended to establish upgradeability for smart contracts - the code could be changed after issue was found in the deployed code. Code upgrade function should be limited to owner account.

### Secure Build and Deployment
- Private keys management process should be established: who has access to owner account, where the owner account and other privileged accounts
- Contract should be compiled then deployed to test network and tested on testnet prior to development to mainnet

## Testing
Testing processes define how-to verify and test the smart contract

### Architecture Assessment
- The architecture design should be reviewed against potential security issues
- Integration tests should be developed and performed

### QA Testing
- Developer team should perform testing against all documented requirements
- Developers should perform internal code review and security audit for the developed codebase
- Automated tests for the code should be developed. The coverage of tests should be at least 70%   

### Security Testing
- The code should be prepared for the audit - documentation, tests, deployments scripts etc.
- The code should be audited by at least 2 independent auditors
- All the issues found during the audit should be fixed. The new version of code should be re-audited
- Putting codebase on bug bounty for 1-2 weeks before deployment is highly recommended
- Third party security consultancy during development is highly recommended
