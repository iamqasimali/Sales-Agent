# SALES-AGENT

**Empowering Smarter Sales Through Seamless Automation**  

![Ruby](https://img.shields.io/badge/Ruby-CC342D?style=for-the-badge&logo=ruby&logoColor=white)
![Rails](https://img.shields.io/badge/Rails-%23CC0000.svg?style=for-the-badge&logo=ruby-on-rails&logoColor=white)
![LLM](https://img.shields.io/badge/LLM-OpenAI-blue?style=for-the-badge&logo=openai&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An intelligent sales automation platform powered by Ruby on Rails and Large Language Models (LLMs) to streamline lead management, customer interactions, and data-driven decision-making.


---

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

---

## Overview
Sales-Agent leverages AI (LLMs) and Rails to automate repetitive sales tasks, including:
- **Lead scoring and prioritization**  
- **Automated email/call responses**  
- **CRM integration**  
- **Conversation analytics**  

Built for scalability with Docker and CI/CD via GitHub Actions.

---

## Features
✅ **AI-Powered Lead Management**  
✅ **Real-Time Customer Insights**  
✅ **Multi-Channel Automation** (Email, SMS, Calls)  
✅ **Rails Admin Dashboard**  
✅ **LLM Integration** (OpenAI/Gemini)  

---

## Getting Started

### Prerequisites
- Ruby **3.2+**  
- Rails **7.0+**  
- PostgreSQL **14+**  
- Docker (optional)  
- OpenAI API key (or other LLM provider)  

### Installation

#### 1. Clone the Repository
```bash
git clone https://github.com/iamqasimali/Sales-Agent
cd Sales-Agent
```

#### 2. Install Dependencies
```bash
bundle install
yarn install
```

#### 3. Database Setup
```bash
rails db:create db:migrate db:seed
```

#### Docker (Alternative)
```bash
docker build -t sales-agent .
docker-compose up
```

---

## Usage
Start the Rails server:
```bash
rails s
```

**Key Commands:**
- Sync leads: `rake sales:sync_leads`  
- Run AI processing: `rake llm:process_conversations`  

Access the dashboard at: `http://localhost:3000/admin`

---

## Configuration
Rename `.env.example` to `.env` and add:
```env
OPENAI_API_KEY=your_key_here
CRM_API_KEY=your_crm_key
```

Configure LLM model in `config/initializers/llm.rb`:
```ruby
Rails.application.config.llm_provider = :openai # or :gemini
```

---

## Testing
Run the test suite:
```bash
bundle exec rspec
```

For integration tests with LLM mocks:
```bash
RAILS_ENV=test bundle exec rspec --tag llm
```

---

## Deployment
**Via Docker:**
```bash
docker-compose -f production.yml up --build
```

**Heroku:**
```bash
heroku container:push web -a your-app-name
```

---

## Contributing
1. Fork the repository  
2. Create a feature branch (`git checkout -b feature/xyz`)  
3. Submit a PR with tests  

---

## License
MIT © [Qasim Ali](https://github.com/iamqasimali)


# Deployment Instructions

Copy the `.env.example` file to `.env` to set up your environment variables. This file contains the necessary configurations for your application.

```
cp .env.example .env
./provision
kamal setup
kamal deploy
```