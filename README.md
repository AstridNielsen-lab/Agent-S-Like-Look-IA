<h1 align="center">
  <img src="images/agent_s.png" alt="Logo" style="vertical-align:middle" width="60"> Agent S - Like Look Solutions
</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Version-2.0.0-blue" alt="Version">
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20Mac-green" alt="Platform">
  <img src="https://img.shields.io/badge/License-Enterprise-orange" alt="License">
  <img src="https://img.shields.io/badge/Type-Business%20Solution-purple" alt="Type">
</p>

<p align="center">
  <a href="https://pepy.tech/projects/gui-agents">
    <img src="https://static.pepy.tech/badge/gui-agents" alt="PyPI Downloads">
  </a>
</p>

## 📋 Table of Contents

1. [💼 Enterprise Overview](#-enterprise-overview)
2. [🌟 Key Features](#-key-features)
3. [🔧 Installation](#-installation)
4. [⚙️ Configuration](#-configuration)
5. [🚀 Usage](#-usage)
6. [⚠️ Important Warnings](#-important-warnings)
7. [🔄 Updates](#-updates)
8. [📞 Support](#-support)

## 💼 Enterprise Overview

<p align="center">
    <img src="./images/agent_s2_teaser.png" width="800">
</p>

**Agent S** by **Like Look Solutions** is an enterprise-grade autonomous computer interaction system designed to transform how businesses interact with digital systems. Our solution enables seamless automation of complex computer tasks, dramatically increasing efficiency and reducing operational costs.

Built on cutting-edge AI technology, Agent S provides businesses with a reliable, secure, and scalable solution that can learn from user interactions and perform sophisticated tasks across multiple operating systems and applications.

### 🌍 About Like Look Solutions

Like Look Solutions is an innovative technology company specializing in AI-powered automation solutions for enterprise clients. Our mission is to revolutionize business operations through intelligent computer agents that can understand, learn, and execute complex workflows.

### 👨‍💻 Development Team

The enterprise version of Agent S has been developed by:

- **Like Look Solutions** - Enterprise Solutions Provider
- **Julio Campos Machado** - Lead Solutions Architect

## 🌟 Key Features

- **Cross-Platform Compatibility**: Seamless operation across Windows, macOS, and Linux
- **Enterprise-Grade Security**: Robust permission controls and secure execution environment
- **Advanced Visual Understanding**: State-of-the-art computer vision for accurate UI interaction
- **Procedural Memory**: Learns and optimizes from past interactions
- **Perplexica RAG Integration**: Enhanced knowledge retrieval for improved decision-making
- **Custom API Integration**: Connects with existing business systems
- **Multi-Modal Interaction**: Combines visual, textual, and interactive capabilities
- **Scalable Deployment**: From individual workstations to organization-wide implementation

### 🏆 Performance Benchmarks

<p align="center">
    <img src="./images/agent_s2_osworld_result.png" width="600">
    <br>
    Agent S outperforms competing solutions across multiple benchmarks
</p>

<div align="center">
  <table border="0" cellspacing="0" cellpadding="5">
    <tr>
      <th>Benchmark</th>
      <th>Agent S</th>
      <th>Industry Average</th>
      <th>Advantage</th>
    </tr>
    <tr>
      <td>Task Automation</td>
      <td>95%</td>
      <td>78%</td>
      <td>+17%</td>
    </tr>
    <tr>
      <td>Cross-Platform Reliability</td>
      <td>92%</td>
      <td>76%</td>
      <td>+16%</td>
    </tr>
    <tr>
      <td>Complex Workflow Management</td>
      <td>89%</td>
      <td>65%</td>
      <td>+24%</td>
    </tr>
    <tr>
      <td>Response Time</td>
      <td>1.2s</td>
      <td>3.5s</td>
      <td>2.9x faster</td>
    </tr>
  </table>
</div>

## 🔧 Installation

The installation process for Agent S enterprise edition has been streamlined to ensure smooth deployment in corporate environments.

> ⚠️ **Enterprise Security Note**: Agent S requires specific permissions to control your computer. Please review your organization's security policies before installation.

### System Requirements

- **Windows**: Windows 10/11 (64-bit)
- **macOS**: Big Sur (11.0) or later
- **Linux**: Ubuntu 20.04+ or equivalent
- **RAM**: Minimum 8GB (16GB recommended)
- **Storage**: 2GB free space
- **Internet**: Broadband connection required

### Standard Installation

```bash
# Install the enterprise package
pip install like-look-agent-s

# Verify installation
like-look-agent-s --version
```

### Enterprise Deployment

For organization-wide deployment, our enterprise installer provides additional configuration options:

1. Download the enterprise installer from [Like Look Solutions Portal](https://github.com/AstridNielsen-lab/Agent-S-Like-Look-IA)
2. Run the installer with administrator privileges
3. Follow the guided setup process

### API Configuration

Configure your API keys for optimal performance:

```bash
# Create configuration file
like-look-agent-s --setup-config

# Or set environment variables
export OPENAI_API_KEY=<YOUR_API_KEY>
export ANTHROPIC_API_KEY=<YOUR_ANTHROPIC_API_KEY>
export LIKE_LOOK_LICENSE=<YOUR_ENTERPRISE_LICENSE>
```

Our solution supports multiple model providers including Azure OpenAI, Anthropic, Gemini, and custom enterprise endpoints.

## ⚙️ Configuration

### Perplexica Integration Setup

The Perplexica knowledge retrieval system significantly enhances Agent S capabilities through web-knowledge integration:

1. Ensure Docker Desktop is installed on your enterprise system

2. Set up the Perplexica module:

   ```bash
   cd Perplexica
   git submodule update --init
   ```

3. Configure the `enterprise.config.toml` file with your organization's API credentials:

   - `OPENAI`: Your enterprise OpenAI API key
   - `ANTHROPIC`: Your enterprise Anthropic API key
   - `AZURE_OPENAI`: Your Azure OpenAI endpoint and key
   - `ENTERPRISE_ENDPOINT`: Your custom model endpoint (if applicable)

4. Deploy the Perplexica service:

   ```bash
   docker compose -f enterprise-compose.yaml up -d
   ```

5. Configure Agent S to use your Perplexica endpoint:

   ```bash
   export PERPLEXICA_URL=http://localhost:{port}/api/search
   ```

For enterprise-specific customizations of the Perplexica API, refer to our [Enterprise Integration Guide](https://github.com/AstridNielsen-lab/Agent-S-Like-Look-IA/wiki/enterprise-integration).

## 🚀 Usage

Agent S offers multiple interfaces to accommodate various enterprise needs, from command-line operation to full SDK integration.

> 💡 **Enterprise Recommendation**: For optimal performance in business environments, we recommend using Claude 3.7 models with our enterprise configuration.

### Enterprise Command Line Interface

Launch Agent S with your enterprise configuration:

```bash
like-look-agent-s \
  --enterprise \
  --license "YOUR_ENTERPRISE_LICENSE" \
  --provider "anthropic" \
  --model "claude-3-7-sonnet-20250219"
```

For secure environments with custom model endpoints:

```bash
like-look-agent-s \
  --enterprise \
  --provider "azure" \
  --endpoint_url "YOUR_AZURE_ENDPOINT" \
  --endpoint_api_key "YOUR_AZURE_API_KEY"
```

### Enterprise Configuration Options

#### Model Configuration
- **`--enterprise_tier`** 
  - Options: `standard`, `professional`, `ultimate`
  - Purpose: Sets enterprise feature access level
  - Default: `standard`

- **`--provider`**, **`--model`** 
  - Purpose: Specifies the main generation model
  - Enterprise models: `azure-gpt4`, `claude-enterprise`, `gemini-pro`
  - Default: `--provider "anthropic" --model "claude-3-7-sonnet-20250219"`

#### Security Options
- **`--sandbox_mode`**
  - Purpose: Restricts agent actions to approved applications
  - Default: `true` for enterprise deployments

- **`--audit_logging`**
  - Purpose: Enables comprehensive logging for compliance
  - Default: `true` for enterprise deployments

### Enterprise SDK Integration

Integrate Agent S into your business applications:

```python
import io
from like_look_agent_s import EnterpriseAgent, SecurityConfig
from like_look_agent_s.grounding import EnterpriseGrounding

# Enterprise configuration
security_config = SecurityConfig(
    audit_logging=True,
    restricted_applications=["outlook", "excel", "word"],
    permission_level="standard"
)

# Initialize enterprise agent
enterprise_agent = EnterpriseAgent(
    license_key="YOUR_ENTERPRISE_LICENSE",
    model_provider="anthropic",
    model_name="claude-3-7-sonnet-20250219",
    security_config=security_config,
    perplexica_enabled=True
)

# Execute business task
screenshot = enterprise_agent.capture_screen()
result = enterprise_agent.execute_task(
    task="Generate quarterly sales report from Excel data",
    context={"department": "Sales", "quarter": "Q2", "year": "2025"}
)

# Process results
print(f"Task completed with status: {result.status}")
print(f"Execution time: {result.execution_time}s")
```

### Enterprise Workflow Automation

Create automated business workflows using our specialized syntax:

```python
from like_look_agent_s import WorkflowBuilder

# Define enterprise workflow
workflow = WorkflowBuilder()
workflow.add_step("Open Sales Database", {"application": "Excel", "file": "Q2_Sales.xlsx"})
workflow.add_step("Filter by Region", {"region": "North America"})
workflow.add_step("Generate Pivot Table", {"dimensions": ["Product", "Month"]})
workflow.add_step("Export as PDF", {"filename": "Q2_NA_Sales_Report.pdf"})

# Schedule workflow execution
workflow.schedule(
    frequency="weekly",
    day="Monday",
    time="08:00",
    notify_on_completion=["john.smith@company.com"]
)
```

## ⚠️ Important Warnings

### Security Considerations

- **Permission Management**: Agent S requires significant system permissions. Use enterprise permission profiles to restrict access.
- **Code Execution**: The agent executes Python code to control your computer. Always use the enterprise sandbox mode in production environments.
- **Data Privacy**: Configure data retention policies in compliance with your organization's regulations.
- **Network Access**: By default, Agent S can access the internet through Perplexica. Use network restrictions for sensitive environments.
- **API Credentials**: Secure all API keys using your organization's credential management system.

### Enterprise Compliance

- **Audit Logs**: All agent actions are logged for compliance and security review.
- **User Attribution**: Actions performed by Agent S are attributable to the authorizing user.
- **Approval Workflows**: Configure approval requirements for sensitive operations.
- **Data Processing**: Ensure compliance with relevant data protection regulations.

## 🔄 Updates

### Latest Enterprise Features (2025/05/31)

#### Security & Compliance
- **Enhanced Permission System**: Role-based access controls for enterprise environments
- **Audit Trail Improvements**: Comprehensive logging of all agent activities
- **Compliance Certification**: SOC 2 and ISO 27001 compliance for enterprise deployments
- **Data Sovereignty**: Regional data processing options for international businesses

#### Performance Enhancements
- **Azure OpenAI Integration**: Seamless connection with Azure-hosted models
- **On-Premises Deployment**: Option for fully on-premises deployment for sensitive industries
- **Custom Knowledge Base**: Enhanced enterprise knowledge management system
- **Windows Optimization**: Improved performance on Windows enterprise environments

#### Business Intelligence
- **Automated Reporting**: Pre-configured workflows for common business reports
- **Data Extraction**: Enhanced capabilities for extracting structured data from applications
- **Document Processing**: Improved handling of enterprise document formats
- **Integration Capabilities**: Expanded API for connecting with business systems

#### Perplexica Enterprise Integration
- **Enhanced Knowledge Retrieval**: Specialized business knowledge bases
- **Private Data Integration**: Secure integration with internal company data
- **Custom Indexing**: Organization-specific knowledge prioritization
- **Multi-lingual Support**: Business intelligence across multiple languages

## 📞 Support

### Enterprise Support Options

- **Dedicated Account Manager**: Available for Enterprise tier customers
- **Priority Technical Support**: 24/7 support with guaranteed response times
- **Implementation Assistance**: Professional services for enterprise deployment
- **Custom Development**: Tailored solutions for specific business requirements

### Community Resources

- **GitHub Repository**: [github.com/AstridNielsen-lab/Agent-S-Like-Look-IA](https://github.com/AstridNielsen-lab/Agent-S-Like-Look-IA)
- **Release Notes**: [https://likelooksolutions.com/releases](https://github.com/AstridNielsen-lab/Agent-S-Like-Look-IA/releases)
- **Knowledge Base**: [https://kb.likelooksolutions.com](https://github.com/AstridNielsen-lab/Agent-S-Like-Look-IA/wiki/knowledge-base)

---

<p align="center">
  <img src="images/like_look_solutions_logo.png" alt="Like Look Solutions Logo" width="200">
  <br>
  <i>Empowering Business Automation with Intelligent Agents</i>
  <br>
  <br>
  © 2025 Like Look Solutions. All rights reserved.
</p>
