# QuoteFlow - Insurance Quote API

Professional life insurance quote calculation platform built with NestJS, GraphQL, and Redis caching.

## Tech Stack
- **NestJS** - Backend framework
- **GraphQL** - API query language
- **Redis** - Caching layer
- **TypeScript** - Type safety
- **Docker** - Containerization

## Features
- Real-time premium calculations
- Risk classification (PREFERRED/STANDARD/HIGH)
- 30-day quote caching
- Input validation
- GraphQL Playground for testing

## Quick Start
```bash
# Install dependencies
npm install

# Start Redis
docker-compose up -d

# Start API
npm run start:dev

Visit http://localhost:3000/graphql for GraphQL Playground.

Sample Query

```graphql
mutation {
  calculateQuote(input: {
    age: 35
    gender: "male"
    coverageAmount: 500000
    healthConditions: ["none"]
    smokingStatus: "non-smoker"
  }) {
    quoteId
    monthlyPremium
    riskClass
  }
}
```
