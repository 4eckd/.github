# CLAUDE.md - AI Assistant Guide for .github Repository

## Repository Overview

This `.github` repository contains organization-level community health files and infrastructure for the **FormerlyIncarcerated.org / Betcartel** ecosystem. It provides standardized templates, discussion frameworks, and community management tools that can be used across all repositories in the organization.

### Repository Purpose
- Organization-wide community health files
- GitHub Discussions infrastructure and templates
- Automated community setup tools
- Contributing guidelines for diverse stakeholder groups
- Security policies and responsible disclosure processes

### Primary Mission
Building dignified, community-driven pathways to opportunity through Web3 technology for formerly incarcerated individuals and their communities.

## Repository Structure

```
.github/
├── COMMUNITY_INFRASTRUCTURE.md    # Overview of discussion infrastructure
├── CONTRIBUTING.md                 # Contribution guidelines for all stakeholders
├── README.md                       # Profile/landing page for @4eckd account
├── SECURITY.md                     # Security policy and researcher profile
├── discussion-categories.yml       # Discussion categories configuration
├── DISCUSSION_TEMPLATE/            # Templates for GitHub Discussions
│   ├── bug-report.md
│   ├── feature-request.md
│   ├── general-discussion.md
│   ├── success-story.md
│   └── welcome-discussions.md
├── ISSUE_TEMPLATE/                 # Templates for GitHub Issues
│   ├── bug_report.yml
│   └── feature_request.yml
├── profile/                        # Organization profile
│   └── README.md
└── scripts/                        # Automation scripts
    ├── setup-community.sh          # Community setup automation
    └── setup-discussions.js        # Discussion categories automation
```

## Core Components

### 1. Discussion Infrastructure (24 Categories across 8 Sections)

The repository defines a comprehensive discussion structure organized into:

#### 📋 Project Management
- Community Announcements (announcement)
- Strategic Discussions (open-ended)
- Community Polls (poll)

#### 🛠️ Technical Development
- Architecture & Design (open-ended)
- Technical Q&A (question/answer)
- Technical Announcements (announcement)

#### 🔐 Web3 & Blockchain
- Blockchain Development (open-ended)
- Security & Privacy (question/answer)
- Security Announcements (announcement)

#### 🐛 Issues & Support
- Help & Support (question/answer)
- Bug Reports & Issues (question/answer)
- Documentation Q&A (question/answer)

#### 🤝 Community & Impact
- General Discussion (open-ended)
- Success Stories (open-ended)
- Impact Polls (poll)

#### 🔬 Research & Innovation
- Research & Development (open-ended)
- Data & Analytics (question/answer)
- Future Vision (open-ended)

#### 🏛️ Governance
- Governance Announcements (announcement)
- Governance Proposals (poll)
- Policy Discussions (open-ended)

#### 💼 Use Cases
- Employment Solutions (open-ended)
- Financial Services (question/answer)
- Housing Solutions (open-ended)

**Reference**: See `discussion-categories.yml:1-132` and `scripts/setup-discussions.js:23-183`

### 2. Templates

#### Discussion Templates (`DISCUSSION_TEMPLATE/`)
- **Feature Request**: Includes Web3 considerations, impact assessment, user stories, acceptance criteria
- **Bug Report**: Environment info, Web3/wallet debugging, privacy sections, reproduction steps
- **Success Story**: Privacy-first sharing, impact measurement, community inspiration
- **General Discussion**: Structured conversation frameworks, inclusive participation

#### Issue Templates (`ISSUE_TEMPLATE/`)
- **bug_report.yml**: Comprehensive YAML-based bug reporting with Web3-specific fields
  - Platform/device information
  - Browser and OS details
  - Web3 wallet integration (MetaMask, WalletConnect, Coinbase Wallet)
  - Blockchain network selection (Ethereum, Polygon, Arbitrum, Base)
  - Transaction hash capture
  - User account type classification
  - Severity assessment

- **feature_request.yml**: Feature proposal template with community input mechanisms

**Reference**: `ISSUE_TEMPLATE/bug_report.yml:1-183` and `DISCUSSION_TEMPLATE/feature-request.md:1-102`

### 3. Automation Scripts

#### `setup-discussions.js` (Node.js)
- GitHub GraphQL API integration for automated discussion category creation
- Creates all 24 discussion categories programmatically
- Error handling for existing categories
- Requires `GITHUB_TOKEN` environment variable with repo permissions
- Uses `@octokit/rest` and `@octokit/graphql` packages
- Configuration for FormerlyIncarcerated organization

**Reference**: `scripts/setup-discussions.js:1-288`

#### `setup-community.sh` (Bash)
- Complete community infrastructure deployment
- GitHub CLI integration and authentication checking
- Discussion enablement automation
- Health checks for community files
- Node.js dependency installation (supports bun and npm)
- Community onboarding support

**Reference**: `scripts/setup-community.sh:1-129`

## Key Stakeholder Groups

When working in this repository, consider these distinct user groups:

1. **Formerly Incarcerated Individuals**
   - Primary beneficiaries
   - Need privacy-first features
   - Success story sharing
   - Clear support pathways

2. **Community Advocates**
   - Support and mentorship roles
   - Impact measurement
   - Feature feedback

3. **Technical Contributors**
   - Developers and technologists
   - Code contributions
   - Security testing
   - Documentation improvements

4. **Organizations & Partners**
   - Employers offering second-chance opportunities
   - Partnership collaborations
   - Sponsorship and funding

## Technology Stack & Conventions

### Languages & Tools
- **JavaScript/TypeScript**: Primary language for automation (prefer TypeScript for new code)
- **Node.js**: Automation scripting
- **Bash**: System-level automation
- **YAML**: Issue templates and configuration
- **Markdown**: Documentation and discussion templates
- **GitHub GraphQL API**: Discussion category management

### Package Managers
- **Primary**: Bun (preferred)
- **Fallback**: npm
- Install dependencies: `bun install` or `npm install`

### Web3 Technologies
- **Blockchains**: Ethereum Mainnet, Polygon, Arbitrum, Base
- **Wallets**: MetaMask, WalletConnect, Coinbase Wallet
- **Smart Contracts**: Solidity
- **Standards**: DeFi integrations, tokenomics, zero-knowledge proofs

**Reference**: `CONTRIBUTING.md:112-118`

### Coding Standards
- Use TypeScript for all new code
- Follow existing code style and formatting
- Write tests for new functionality
- Ensure accessibility compliance (WCAG 2.1 AA)
- Test across all supported themes (6 theme system)

**Reference**: `CONTRIBUTING.md:112-118`

## Development Workflow

### Setting Up Community Infrastructure

1. **Enable GitHub Discussions**
   ```bash
   gh repo edit <owner>/<repo> --enable-discussions
   ```

2. **Install Dependencies**
   ```bash
   bun install  # or npm install
   ```

3. **Set Environment Variables**
   ```bash
   export GITHUB_TOKEN=<your_token_with_repo_permissions>
   ```

4. **Run Automated Setup**
   ```bash
   # Create discussion categories
   node scripts/setup-discussions.js

   # Or run complete setup
   ./scripts/setup-community.sh
   ```

### Pull Request Process
1. Ensure code follows style guidelines
2. Add tests for new features
3. Update documentation as needed
4. Submit PR with clear description
5. Respond to code review feedback promptly

**Reference**: `CONTRIBUTING.md:120-126`

## Security Considerations

### Security Research Focus
This organization has a strong security research background, particularly in:
- Web3 security auditing
- Smart contract analysis and vulnerability assessment
- Blockchain forensics
- Authentication bypass vulnerabilities
- Privacy-focused implementations

### Reporting Security Issues
- **Email**: security@betcartel.io
- **DO NOT** create public issues for security vulnerabilities
- Provide detailed information about the issue
- Allow time for investigation and resolution
- Follow responsible disclosure practices

### Security Best Practices
- Keep dependencies updated
- Follow secure coding practices
- Use proper authentication and authorization
- Protect sensitive user data
- Never commit secrets or credentials
- Implement privacy-by-design principles

**Reference**: `CONTRIBUTING.md:159-174` and `SECURITY.md:1-102`

### Notable Security Research Areas (2025)
- Deceptive event emissions in smart contracts
- Hidden token redirection mechanisms
- Authentication bypass vulnerabilities
- API security and data leakage
- Blockchain transaction analysis
- Smart contract decompilation

**Reference**: `SECURITY.md:70-98`

## Community Guidelines

### Respectful Communication
- Be respectful and inclusive in all interactions
- Use welcoming and professional language
- Respect diverse perspectives and experiences
- Avoid discriminatory or offensive language

### Privacy and Safety
- Respect privacy and confidentiality
- Don't share personal information without consent
- Be mindful of sensitive topics related to incarceration
- Report harassment or inappropriate behavior

### Constructive Participation
- Focus on solutions and positive outcomes
- Provide constructive feedback
- Help others learn and grow
- Celebrate community successes

**Reference**: `CONTRIBUTING.md:128-157`

## Labels and Organization

### Priority Labels
- `priority: critical` - Urgent issues requiring immediate attention
- `priority: high` - Important for current sprint
- `priority: medium` - Standard priority items
- `priority: low` - Nice-to-have improvements

### Type Labels
- `type: bug` - Something isn't working
- `type: feature` - New feature or enhancement
- `type: documentation` - Documentation improvements
- `type: security` - Security-related issues

### Component Labels
- `component: frontend` - Frontend/UI related
- `component: backend` - Backend/API related
- `component: blockchain` - Smart contracts/Web3
- `component: identity` - Identity system

**Reference**: `CONTRIBUTING.md:176-200`

## Communication Channels

### Official Channels
- **General**: hello@betcartel.io
- **Technical Support**: support@betcartel.io
- **Security**: security@betcartel.io
- **Partnerships**: partnerships@betcartel.io
- **Discord**: https://discord.gg/m3WwmkMHAx
- **Documentation**: https://docs.betcartel.io

### GitHub Resources
- **Discussions**: Organization-level and repository-level
- **Issues**: Bug reports and feature requests
- **Pull Requests**: Code contributions

**Reference**: `CONTRIBUTING.md:202-215`

## AI Assistant Guidelines

### When Working in This Repository

1. **Understand the Context**
   - This is a community infrastructure repository
   - Focus on social impact and empowerment
   - Respect privacy and sensitivity around incarceration topics

2. **Emoji Usage**
   - Emojis are extensively used in this codebase
   - They improve visual organization and accessibility
   - Follow existing emoji patterns in templates and categories
   - Use consistently across similar document types

3. **Template Modifications**
   - Preserve existing structure and field organization
   - Maintain Web3-specific sections
   - Keep privacy and security considerations prominent
   - Ensure accessibility compliance

4. **Script Updates**
   - Test with both bun and npm
   - Maintain error handling patterns
   - Preserve GitHub API authentication flows
   - Update environment variable documentation

5. **Documentation Standards**
   - Use clear, professional language
   - Include practical examples
   - Consider all stakeholder groups
   - Link to related resources
   - Keep formatting consistent

6. **Privacy First**
   - Never expose sensitive personal information
   - Maintain privacy-focused defaults
   - Consider anonymization options
   - Respect confidentiality needs

7. **Web3 Integration**
   - Understand blockchain networks in use
   - Include wallet compatibility considerations
   - Support transaction tracking and debugging
   - Consider gas fees and network congestion

8. **Testing Considerations**
   - Test discussion category creation
   - Validate template rendering
   - Check GitHub API permissions
   - Verify cross-platform compatibility

## Success Metrics

### Engagement Metrics
- Discussion participation rates across categories
- Community member growth and retention
- Success story sharing frequency
- Poll participation and feedback quality

### Quality Metrics
- Template usage rates for discussions and issues
- Category distribution and balanced usage
- Resolution rates for questions and issues
- Community satisfaction and feedback scores

### Impact Metrics
- Formerly incarcerated individual participation
- Employment and business success stories
- Community support and mentorship connections
- Platform improvement suggestions implemented

**Reference**: `COMMUNITY_INFRASTRUCTURE.md:163-182`

## File Reference Quick Guide

### Primary Documentation
- `CONTRIBUTING.md:1-235` - Complete contribution guide
- `COMMUNITY_INFRASTRUCTURE.md:1-207` - Infrastructure overview
- `README.md:1-135` - Profile and navigation
- `SECURITY.md:1-102` - Security policy and research profile

### Configuration Files
- `discussion-categories.yml:1-132` - Discussion structure definition

### Templates
- `ISSUE_TEMPLATE/bug_report.yml:1-183` - Structured bug reporting
- `ISSUE_TEMPLATE/feature_request.yml` - Feature proposals
- `DISCUSSION_TEMPLATE/feature-request.md:1-102` - Feature discussions
- `DISCUSSION_TEMPLATE/bug-report.md` - Bug discussions
- `DISCUSSION_TEMPLATE/success-story.md` - Impact stories
- `DISCUSSION_TEMPLATE/general-discussion.md` - General conversations

### Automation
- `scripts/setup-discussions.js:1-288` - Node.js automation
- `scripts/setup-community.sh:1-129` - Bash automation

## Common Tasks

### Adding a New Discussion Category

1. Update `discussion-categories.yml` with new category definition
2. Add category to `scripts/setup-discussions.js` categories array
3. Create corresponding discussion template in `DISCUSSION_TEMPLATE/` if needed
4. Run setup script to create category: `node scripts/setup-discussions.js`
5. Update documentation in `COMMUNITY_INFRASTRUCTURE.md`

### Creating a New Issue Template

1. Create YAML file in `ISSUE_TEMPLATE/` directory
2. Follow existing template structure (see `bug_report.yml`)
3. Include Web3-specific fields if applicable
4. Add user type classification options
5. Include privacy and security considerations
6. Test template rendering on GitHub

### Updating Automation Scripts

1. Maintain backward compatibility with existing deployments
2. Update both Node.js and Bash scripts if applicable
3. Test with different package managers (bun and npm)
4. Verify GitHub API permissions and rate limits
5. Update environment variable documentation
6. Add error handling for new failure modes

### Modifying Community Guidelines

1. Consider impact on all stakeholder groups
2. Maintain privacy-first approach
3. Ensure inclusive language
4. Update related documentation
5. Announce changes in Community Announcements category

## Related Repositories

This `.github` repository supports the broader ecosystem:
- Main project repositories use these templates
- Organization profile inherits these health files
- All repositories benefit from discussion infrastructure
- Security policies apply across organization

## License

By contributing to this repository, you agree that your contributions will be licensed under the same license as the respective project.

---

**Last Updated**: 2025-11-15

**Maintained By**: @jlucus / @4eckd

**Mission**: Building second chances through Web3 technology and community-driven support systems.

**For Questions**: Review `CONTRIBUTING.md` or reach out via official communication channels listed above.
