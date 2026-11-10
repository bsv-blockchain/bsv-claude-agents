# @bsv/bsv-claude-agents - BSV Claude Agents Installer

[![NPM Version](https://img.shields.io/npm/v/@bsv/bsv-claude-agents)](https://www.npmjs.com/package/@bsv/bsv-claude-agents)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache--2.0-blue.svg)](https://github.com/bsv-blockchain/bsv-claude-agents/blob/main/LICENSE)

This package provides BSV (Bitcoin SV) expert Claude agents for Claude Code. It automatically installs and manages BSV blockchain development agents that provide specialized knowledge and assistance for BSV application development.

## Features

- **Easy Installation**: One-command setup via npx
- **Expert BSV Agents**: Three specialized agents for BSV development: TypeScript SDK, wallet toolbox, and identity services
- **Automatic Updates**: Re-run the command to update agents
- **Symlink Management**: Clean installation and removal of agent files

## Quick Start

Install or update BSV Claude agents:

```bash
// If not installed in project
npx @bsv/bsv-claude-agents
// If installed in project
npx bsv-claude-agents
```

That's it! The BSV agents are now available in your Claude Code interface.

## What Gets Installed

This package installs the following BSV expert agents:

### BSV Blockchain TypeScript SDK Expert
- **File**: `bsv-blockchain-ts-sdk-expert.md`
- **Expertise**: Complete BSV ecosystem including transaction building, script creation, SPV verification, merkle proofs, ARC broadcasting, BRC standards implementation, threshold signatures, secret sharing, wallet integration, overlay networks, identity management, and distributed storage
- **Use Cases**: Building BSV applications with TypeScript/JavaScript, advanced cryptographic operations, enterprise-scale blockchain solutions, P2PKH templates, custom scripts, fee calculation
- **Note**: Some advanced features may require direct repository access

### BSV Blockchain Wallet Toolbox Expert
- **File**: `bsv-blockchain-wallet-toolbox-expert.md`
- **Expertise**: Wallet functionality, transaction creation, key management, address generation, UTXO handling
- **Use Cases**: Implementing BSV wallet features, transaction signing, UTXO management, BRC-100 compliance

### BSV Blockchain Identity Services Expert
- **File**: `bsv-blockchain-identity-services-expert.md`
- **Expertise**: Production-scale BSV Overlay Services architecture, identity certificate validation, Topic Manager implementation, Lookup Service patterns, BRC-64/65 standards, comprehensive testing strategies, deployment automation, and advanced database optimization
- **Use Cases**: Building robust identity verification systems, certificate registries, privacy-enhanced identity solutions, production-scale overlay networks, enterprise identity management

## How to Use BSV Agents in Claude Code

After installation, the BSV agents become available as specialized assistants in Claude Code. Here's how to use them effectively:

### Invoking BSV Agents

#### Automatic Agent Selection
Claude Code will often automatically suggest the most appropriate BSV agent based on your task description. For example:
- "Help me build a BSV transaction" → Suggests `bsv-blockchain-ts-sdk-expert`
- "I need to implement wallet functionality" → Suggests `bsv-blockchain-wallet-toolbox-expert`
- "Create an identity certificate system" → Suggests `bsv-blockchain-identity-services-expert`

#### Manual Agent Invocation
You can explicitly invoke an agent using the Task tool in Claude Code. Simply describe your task and Claude will route it to the appropriate agent:

```
User: "I need to create a P2PKH transaction with the BSV SDK"
Claude: [Uses Task tool with bsv-blockchain-ts-sdk-expert]
```

### When to Use Each Agent

#### BSV Blockchain TypeScript SDK Expert
**Best for:**
- Low-level blockchain interactions using `@bsv/sdk`
- Custom script logic and OP_RETURN data
- SPV verification and merkle proofs
- BRC standards implementation (BRC-42, BRC-29, BRC-62, BRC-78, BRC-95)
- BEEF format and transaction broadcasting via ARC
- Distributed storage with SHIP protocol
- Advanced cryptographic operations (threshold signatures, secret sharing)
- Wallet integration with substrate patterns
- Overlay networks and identity management
- Enterprise-scale blockchain solutions

**Example scenarios:**
```
"Generate TypeScript code to create a P2PKH transaction sending 10,000 satoshis"
"How do I embed data in a transaction using OP_RETURN?"
"Implement SPV verification for a transaction using MerklePath"
"Show me BRC-42 key derivation for a specific protocol ID"
"Create a 3-of-5 threshold signature system using KeyShares"
"Implement secret sharing with Polynomial operations"
"Set up overlay network broadcasting with TopicBroadcaster"
"Build enterprise wallet integration using WalletWire protocol"
"Create atomic BEEF transactions for batch processing"
```

#### BSV Blockchain Wallet Toolbox Expert
**Best for:**
- Complete wallet implementation using `@bsv/wallet-toolbox`
- Key management and secure storage
- UTXO management and selection
- Service integration (ARC, WhatsOnChain, Dojo)
- Multi-environment deployment (server, browser, mobile)
- BRC-100 wallet compliance
- Background synchronization with MonitorDaemon

**Example scenarios:**
```
"Set up a BSV wallet for a web app with IndexedDB storage"
"List spendable UTXOs and construct a payment transaction"
"Implement background monitoring for wallet synchronization"
"Handle WERR_* error codes in wallet operations"
```

#### BSV Blockchain Identity Services Expert
**Best for:**
- Production-scale decentralized identity systems
- BRC-64/65 certificate management with comprehensive validation
- BSV Overlay Services architecture and deployment
- Topic Manager implementation with robust validation logic
- Lookup Service patterns with advanced database optimization
- PushDrop encoding for secure on-chain storage
- Privacy-enhanced identity with field encryption
- Comprehensive testing strategies for identity systems
- Deployment automation and production monitoring
- Enterprise identity management at scale

**Example scenarios:**
```
"Design a BRC-64/65 compliant identity certificate schema"
"Implement a TopicManager for validating identity certificates"
"Query identity records in a LookupService using MongoDB"
"Encode a VerifiableCertificate on-chain using PushDrop"
"Build a production-scale overlay network for identity verification"
"Implement comprehensive testing for identity certificate validation"
"Set up deployment automation for identity services"
"Optimize database queries for large-scale identity lookups"
"Create enterprise identity management with monitoring and alerts"
```

### Working with Multiple Agents

For complex BSV projects, you'll often need to combine expertise from multiple agents:

#### Identity-Enabled Wallet
Combine `identity-services` and `wallet-toolbox` agents:
1. Use identity agent to design BRC-64/65 certificates
2. Use wallet agent to integrate identity storage and signing

#### Custom Transaction in a Wallet
Combine `ts-sdk` and `wallet-toolbox` agents:
1. Use wallet agent for UTXO selection and key management
2. Use SDK agent for custom script creation and transaction building

#### Full dApp Development
Use all three agents together:
1. Identity agent for user authentication layer
2. Wallet agent for fund management
3. SDK agent for custom smart contracts and protocols

#### Enterprise-Scale Production Deployment
Combine all agents for production-ready systems:
1. **SDK agent** for advanced cryptographic operations, threshold signatures, and enterprise blockchain infrastructure
2. **Identity agent** for production-scale overlay networks, comprehensive testing, and deployment automation
3. **Wallet agent** for enterprise wallet management with monitoring and error handling

#### High-Throughput Transaction Processing
Leverage advanced capabilities across agents:
1. **SDK agent** for atomic BEEF transactions, batch processing, and enterprise broadcasting
2. **Wallet agent** for optimized UTXO management and concurrent transaction handling
3. **Identity agent** for certificate validation at scale and database optimization

### Best Practices

1. **Be Specific**: Provide detailed requirements and context for better results
2. **Include Code Context**: Share existing code snippets or architecture decisions
3. **Iterate and Refine**: Use agent outputs as starting points and request modifications
4. **Choose the Right Agent**: Match the agent to your specific task domain
5. **Combine Strategically**: Break complex tasks into sub-problems for each agent

#### Enterprise Development Considerations

6. **Production Readiness**: Leverage agents' production-scale features for enterprise deployments
7. **Testing Strategy**: Use identity agent's comprehensive testing capabilities for robust validation
8. **Deployment Automation**: Implement deployment automation patterns for consistent releases
9. **Performance Optimization**: Apply database optimization and scaling patterns for high-throughput systems
10. **Security Best Practices**: Implement threshold signatures and advanced cryptographic operations for enterprise security
11. **Monitoring and Alerting**: Build production monitoring into identity and wallet systems
12. **Error Handling**: Implement comprehensive error handling patterns across all agent integrations

## How It Works

1. **Clones Repository**: Downloads the latest BSV agents from GitHub
2. **Creates Symlinks**: Links agent files to your `~/.claude/agents/` directory  
3. **Preserves Updates**: Maintains connection to source repository for easy updates
4. **Clean Management**: Handles existing files and provides clean installation

The agents are installed as symlinks from `~/.claude/bsv-claude-agents/agents/` to `~/.claude/agents/`, allowing for easy updates and management.

## Requirements

- **Node.js**: Version 14 or higher
- **Git**: Required for cloning the agents repository
- **Claude Code**: The agents are designed for use with Claude Code

### Windows Users
The package is fully compatible with Windows! The CLI automatically detects your operating system and uses the appropriate linking method:
- **Windows**: Uses hard links (no administrator privileges required)
- **macOS/Linux**: Uses symbolic links (standard approach)

If you encounter permission issues on Windows, you can:
- Enable Developer Mode in Windows Settings → Update & Security → For developers
- Or run the command as administrator (not recommended for regular use)

## Update Agents

To update your BSV agents to the latest version, simply run the installation command again:

```bash
// If not installed in project
npx @bsv/bsv-claude-agents
// If installed in project
npx bsv-claude-agents
```

This will pull the latest changes and update your local agent files.

## Development

For local development and testing:

```bash
git clone https://github.com/bsv-blockchain/bsv-claude-agents.git
cd bsv-claude-agents
node bin/cli.js --local
```

## Troubleshooting

### Windows Issues
If you encounter linking errors on Windows:
1. **Try Developer Mode**: Enable Developer Mode in Windows Settings
2. **Check File System**: Ensure you're using NTFS (required for hard links)
3. **Fallback Mode**: The CLI automatically falls back to file copying if linking fails

### General Issues
- **Git not found**: Ensure Git is installed and available in your PATH
- **Permission errors**: Check that you have write access to `~/.claude/` directory
- **Node.js version**: Verify you're using Node.js 14 or higher

## Support

- **Documentation**: [BSV Blockchain Documentation](https://docs.bsvblockchain.org/)
- **Issues**: [GitHub Issues](https://github.com/bsv-blockchain/bsv-claude-agents/issues)
- **Community**: [BSV Developer Community](https://discord.gg/bsv)

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.