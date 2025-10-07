# Loom Video Scripts - Staking Feature Code Deep Dive (2 Minutes Each)

## 🎬 Video 1: Smart Contract Development & Testing (2 minutes)

### **Title:** "Building STX Staking Smart Contract - From Code to Tests"

### **Script:**

**[0:00 - 0:15] Hook**

> "Let me show you how I built a production-ready STX staking smart contract with comprehensive testing using Clarinet."

**[0:15 - 0:45] Smart Contract Code**

> "Here's the Clarity contract - four core functions with proper error handling. Notice the input validation and the `as-contract` pattern for STX transfers."
>
> _[Show staking.clar - highlight key functions, error constants, and validation patterns]_

**[0:45 - 1:15] Testing with Clarinet**

> "The real magic is in testing. Watch this - `clarinet check` validates syntax, then our comprehensive test suite covers all edge cases..."
>
> _[Terminal demo: clarinet check, then clarinet test showing all tests passing]_

**[1:15 - 1:45] Test Coverage**

> "Look at these tests - we cover successful staking, insufficient funds, unauthorized unstaking, and edge cases. This caught several bugs during development."
>
> _[Quick scroll through tests/staking_test.ts showing different test scenarios]_

**[1:45 - 2:00] Wrap-up**

> "Solid testing foundation means confident deployment. Next video: deployment to testnet!"

---

## 🎬 Video 2: Deployment Process & Configuration (2 minutes)

### **Title:** "Deploying STX Staking Contract: Clarinet to Testnet"

### **Script:**

**[0:00 - 0:15] Introduction**

> "Time to deploy! Here's the complete process from local development to live testnet deployment."

**[0:15 - 0:45] Deployment Configuration**

> "First, generate the deployment plan with `clarinet deployments generate --testnet --medium-cost`. This creates our testnet-plan.yaml with proper fee estimation."
>
> _[Show terminal command and generated deployment plan file]_

**[0:45 - 1:15] Live Deployment**

> "Deploy with `clarinet deployments apply -p testnet-plan.yaml`. Watch the transaction broadcast and confirmation - costs about 0.31 STX."
>
> _[Terminal demo showing actual deployment process and transaction ID]_

**[1:15 - 1:45] Environment Configuration**

> "After deployment, update .env with the contract address. The frontend automatically switches from mock data to real blockchain calls."
>
> _[Show .env.local update and code that detects contract deployment]_

**[1:45 - 2:00] Wrap-up**

> "Contract is live! Next video: the frontend integration that makes it all work together."

---

## 🎬 Video 3: Frontend Integration Architecture (2 minutes)

### **Title:** "Frontend Integration: Mock Data to Live Blockchain"

### **Script:**

**[0:00 - 0:15] Introduction**

> "Here's how I built the frontend integration that seamlessly switches between mock data and live blockchain calls."

**[0:15 - 0:45] Integration Layer**

> "The magic is in this staking-contract.ts file - it detects if contracts are deployed and falls back to mock data during development. Look at this error handling pattern."
>
> _[Show lib/staking-contract.ts with mock data fallbacks and error handling]_

**[0:45 - 1:15] Custom Hook Architecture**

> "The use-staking hook manages all blockchain state and automatically syncs with wallet connections. Notice how it handles loading states and errors gracefully."
>
> _[Show hooks/use-staking.ts highlighting state management and wallet integration]_

**[1:15 - 1:45] Component Structure**

> "Components stay focused on UI - all blockchain logic is abstracted into the hook. This makes testing easier and components more reusable."
>
> _[Quick show of component structure and how they consume the hook]_

**[1:45 - 2:00] Wrap-up**

> "Mock data during development was a game-changer - build UI fast, then connect to real contracts. Final video: see it all working!"

---

## 🎬 Video 4: Live Demo & Final Result (2 minutes)

### **Title:** "STX Staking Platform: From Code to Working DApp"

### **Script:**

**[0:00 - 0:15] Introduction**

> "Let's see everything working together - from smart contract to live staking interface."

**[0:15 - 0:45] Contract Verification**

> "First, let's verify our deployed contract is working. Using Clarinet console to call functions directly on testnet..."
>
> _[Terminal demo: clarinet console, call contract functions, show successful responses]_

**[0:45 - 1:15] Live Staking Demo**

> "Now the frontend - connect wallet, stake some STX, check balance updates. Notice how it seamlessly integrates with the deployed contract."
>
> _[Quick UI demo: wallet connection, stake transaction, balance update]_

**[1:15 - 1:45] Code to Production**

> "From 200 lines of Clarity code to a full DeFi platform. The testing with `clarinet check` and comprehensive test suite gave me confidence to deploy."
>
> _[Show final code structure and mention key files]_

**[1:45 - 2:00] Wrap-up**

> "Complete code walkthrough done! Smart contract, tests, deployment, and frontend integration. All code is open source - links below!"

---

## 📋 Recording Tips & Setup

### **Pre-Recording Checklist:**

- [ ] Clean desktop/browser
- [ ] Close unnecessary applications
- [ ] Test audio levels
- [ ] Prepare demo data/accounts
- [ ] Have all files ready to open
- [ ] Test screen recording software

### **Recording Setup:**

- **Resolution:** 1920x1080 minimum
- **Frame Rate:** 30fps
- **Audio:** Clear microphone, no background noise
- **Cursor:** Enable cursor highlighting
- **Zoom:** Use browser zoom for better visibility of code

### **Editing Notes:**

- Add captions for accessibility
- Include timestamps in description
- Add relevant links in description
- Create custom thumbnail with code/UI preview
- Add intro/outro with subscribe reminder

### **Description Template:**

```
🚀 In this video, I walk through [specific topic]

⏰ Timestamps:
0:00 Introduction
[Add specific timestamps]

🔗 Useful Links:
- GitHub Repository: [link]
- Deployment Guide: [link]
- Clarinet Documentation: https://docs.hiro.so/clarinet
- Stacks Documentation: https://docs.stacks.co

💻 Tech Stack:
- Clarity Smart Contracts
- Clarinet Testing Framework
- Next.js 15 & React 19
- @stacks/transactions
- Stacks Blockchain

🛠️ Key Commands Shown:
- clarinet check
- clarinet test
- clarinet deployments generate --testnet
- clarinet deployments apply

#Stacks #Clarity #SmartContracts #Clarinet #Web3 #Blockchain
```

### **Engagement Strategy:**

- Ask viewers to comment with questions
- Encourage them to try building similar features
- Offer to review their code in future videos
- Create follow-up videos based on comments
- Pin a comment with additional resources
