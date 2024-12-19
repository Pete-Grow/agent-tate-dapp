# Agent Tate DApp

## Overview

Agent Tate is a groundbreaking decentralized application that combines autonomous AI agency with community-driven social interaction. Built on the Solana blockchain, the platform creates an ecosystem where an AI agent interacts with and learns from its community while maintaining autonomous decision-making capabilities.

### Core Features

The platform integrates several innovative components to create a unique user experience:

- **Autonomous AI Agent:** Powered by the CrewAI framework and Mixtral-8x7b model, providing intelligent interactions and decision-making
- **Community-Driven Development:** Users can influence the agent's actions through a sophisticated reputation-based suggestion system
- **On-Chain Identity System:** Comprehensive Web3 identity and reputation tracking
- **AI-Driven Mentorship:** Personalized guidance and learning paths for community members
- **Token Economics:** Built on Solana using pump.fun for efficient token mechanics

## Project Structure

The project follows a modular architecture designed for scalability and maintainability:

```
agent-tate-dapp/
├── frontend/               # React-based web interface
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── hooks/        # Custom React hooks
│   │   ├── pages/        # Page components
│   │   └── utils/        # Utility functions
│   └── public/           # Static assets
├── backend/               # Backend services
│   ├── agent_core/       # AI agent implementation
│   ├── reputation/       # Reputation system
│   ├── content/          # Content management
│   └── blockchain/       # Blockchain integration
├── contracts/            # Solana smart contracts
│   ├── token/           # Token and staking contracts
│   └── governance/      # Governance system
└── docs/                 # Documentation
    ├── api/             # API documentation
    ├── contracts/       # Smart contract documentation
    └── deployment/      # Deployment guides
```

## Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v16 or later)
- Python 3.9+
- Rust (for Solana contract development)
- Solana CLI tools
- Docker and Docker Compose

### Local Development Setup

1. Clone the repository:
```bash
git clone https://github.com/Pete-Grow/agent-tate-dapp.git
cd agent-tate-dapp
```

2. Install dependencies:
```bash
# Frontend dependencies
cd frontend
npm install

# Backend dependencies
cd ../backend
poetry install

# Smart contract dependencies
cd ../contracts
cargo build
```

3. Set up environment variables:
```bash
# Copy example environment files
cp .env.example .env
```

4. Start development servers:
```bash
# Start frontend development server
cd frontend
npm run dev

# Start backend services
cd ../backend
poetry run uvicorn main:app --reload

# Deploy local test contracts
cd ../contracts
solana-test-validator
solana program deploy ./target/deploy/agent_token.so
```

## Contributing

We welcome contributions from the community! Please read our Contributing Guidelines before submitting pull requests.

### Development Guidelines

1. Code Style
- Frontend: Follow React best practices and use TypeScript
- Backend: Follow PEP 8 guidelines for Python code
- Smart Contracts: Follow Solana program best practices

2. Testing
- Write unit tests for all new features
- Ensure all tests pass before submitting PRs
- Include integration tests for major features

3. Documentation
- Update relevant documentation for new features
- Include inline comments for complex logic
- Update the README if necessary

## Deployment

### Production Deployment

1. Smart Contracts:
```bash
solana program deploy ./target/deploy/agent_token.so
```

2. Backend Services:
```bash
docker-compose up -d
```

3. Frontend:
```bash
npm run build
npm run deploy
```

### Environment Variables

Required environment variables for deployment:
- `SOLANA_RPC_URL`: Solana RPC endpoint
- `MIXTRAL_API_KEY`: API key for AI model
- `PUMP_FUN_API_KEY`: pump.fun API key
- `DATABASE_URL`: Database connection string

## Security

Please report any security vulnerabilities to security@agenttate.com. We take all security concerns seriously.

### Security Measures

- Smart contract audits
- Regular security updates
- Input validation and sanitization
- Rate limiting
- Data encryption

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support and questions:
- Create an issue in the GitHub repository
- Join our Discord community
- Email support@agenttate.com

## Acknowledgments

Special thanks to:
- The CrewAI team for their framework
- The Solana Foundation
- The pump.fun team
- All our contributors and community members