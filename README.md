# AI-Powered GitHub Issues to Notion Workflow

An intelligent n8n automation that transforms GitHub issue management by automatically syncing issues to Notion with AI-powered summarization and enrichment.

![n8n Workflow Diagram](image.png)

## 🌟 Overview

This workflow creates a seamless bridge between **GitHub** and **Notion**, leveraging **Google Gemini AI** to automatically process, summarize, and organize GitHub issues into a structured Notion database. Perfect for teams who want to centralize their issue tracking and project management.

## 🔧 How It Works

The workflow consists of 4 main components:

1. **🔗 GitHub Trigger**: Monitors your repository for new or updated issues
2. **🤖 AI Agent**: Uses Google Gemini to intelligently summarize and structure issue data
3. **📋 Structured Output Parser**: Formats the AI response into consistent JSON structure
4. **📊 Notion Database**: Creates organized pages with enriched issue information

### Workflow Process:

1. **Issue Detection** → GitHub webhook triggers when issues are created/updated
2. **AI Processing** → Gemini AI analyzes the issue and creates:
   - Concise summary
   - Actionable items
   - Additional context notes
3. **Data Structuring** → Output is formatted with repository metadata
4. **Notion Creation** → Structured data becomes a new Notion database page

## 📊 Notion Database Structure

The workflow creates Notion pages with the following properties:

| Column Name          | Type     | Description                    |
|---------------------|----------|--------------------------------|
| **Title**           | Title    | Issue title from GitHub       |
| **Summary**         | Text     | AI-generated concise summary  |
| **Action Items**    | Text     | Key tasks and next steps      |
| **Notes**           | Text     | Additional context            |
| **Repository**      | Text     | Repository name               |
| **Repository URL**  | URL      | Direct link to repository     |
| **Status**          | Select   | Issue state (open/closed)     |
| **Last Activity**   | Date     | Last update timestamp         |
| **Assigned To**     | Text     | GitHub assignee information   |

## 🚀 Setup Instructions

### Prerequisites

- n8n instance (cloud or self-hosted)
- GitHub repository access
- Notion workspace
- Google Gemini API access

### Step 1: GitHub API Setup

1. **Generate Personal Access Token**:
   - Go to GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
   - Click "Generate new token (classic)"
   - Name: `n8n-integration`
   - Scopes: Select `repo` (full repository access)
   - Copy the generated token

2. **Configure n8n Credentials**:
   - In n8n → Credentials → New Credential → GitHub API
   - Authentication method: Access Token
   - Paste your token and save

### Step 2: Google Gemini API Setup

1. **Get API Key**:
   - Visit [Google AI Studio](https://makersuite.google.com/app/apikey)

   - Create new API key
   - Copy the key

2. **Configure n8n Credentials**:
   - In n8n → Credentials → New Credential → Google PaLM API
   - Paste your API key and save

### Step 3: Notion API Setup

1. **Create Integration**:
   - Go to [Notion Integrations](https://www.notion.com/my-integrations)
   - Click "New integration"
   - Fill in details and enable capabilities:
     - ✅ Read content
     - ✅ Update content  
     - ✅ Insert content
   - Copy the Internal Integration Token

2. **Create Notion Database**:
   - Create a new database in Notion
   - Add the columns as specified in the table above
   - Share the database with your integration

3. **Configure n8n Credentials**:
   - In n8n → Credentials → New Credential → Notion API
   - Paste your integration token and save

### Step 4: Import and Configure Workflow

1. **Import Workflow**:
   - Download `Github issue to notion database page.json`
   - In n8n → Import from file
   - Select the JSON file

2. **Configure Nodes**:
   - **GitHub Trigger**: Select your credentials and repository
   - **Google Gemini Chat Model**: Select your Gemini credentials
   - **Notion Node**: Select your credentials and target database

3. **Activate Workflow**:
   - Test the workflow with a sample issue
   - Activate for continuous monitoring

## 🎯 Features

- **🤖 AI-Powered Summarization**: Intelligent analysis of issue content
- **📊 Structured Data**: Consistent formatting for easy tracking
- **🔄 Real-time Sync**: Automatic updates when issues change
- **🏷️ Rich Metadata**: Repository info, timestamps, and assignee tracking
- **📋 Action Items**: AI-extracted tasks and next steps
- **🔗 Direct Links**: Quick access to original GitHub issues

## 💡 Use Cases

- **Project Management**: Centralize issue tracking across multiple repositories
- **Team Coordination**: Keep stakeholders informed with AI summaries
- **Sprint Planning**: Organized view of issues with action items
- **Progress Tracking**: Monitor issue lifecycle and updates
- **Documentation**: Maintain structured records of development tasks

## 🛠️ Customization

You can customize the workflow by:

- **Modifying AI Prompts**: Adjust the summary style and focus areas
- **Adding Fields**: Include additional GitHub metadata
- **Filtering Issues**: Add conditions to process specific issue types
- **Notification**: Connect to Slack, email, or other services

## 📋 Troubleshooting

**Common Issues:**

1. **GitHub Webhook Not Triggering**:
   - Verify repository permissions
   - Check webhook URL in GitHub settings

2. **Notion Pages Not Created**:
   - Ensure database is shared with integration
   - Verify column names match exactly

3. **AI Responses Inconsistent**:
   - Review and refine the prompt in AI Agent node
   - Check Google Gemini API quota

## Set up steps

- Takes about **10–15 minutes** to set up  
- You'll need:
  - A **GitHub token** (for repo access)  
  - A **Notion API token** (with database shared)  
  - A **Google Gemini API key**  
- Configure the **GitHub Trigger**, **AI Agent**, and **Notion Database node**  
- Activate the workflow, and you're done 🚀  

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

⭐ **Star this repository** if you find it helpful! 

💬 **Questions?** Open an issue or reach out to [AkilLabs](https://github.com/AkilLabs)

3. **Activate Workflow**:

### Step 2: Google Gemini API Setup   - Test the workflow with a sample issue

   - Activate for continuous monitoringAn intelligent n8n automation that transforms GitHub issue management by automatically syncing issues to Notion with AI-powered summarization and enrichment.

1. **Get API Key**:

   - Visit [Google AI Studio](https://makersuite.google.com/app/apikey)![n8n Workflow Diagram](image.png)

   - Create new API key

   - Copy the key## 🌟 Overview



2. **Configure n8n Credentials**:This workflow creates a seamless bridge between **GitHub** and **Notion**, leveraging **Google Gemini AI** to automatically process, summarize, and organize GitHub issues into a structured Notion database. Perfect for teams who want to centralize their issue tracking and project management.

   - In n8n → Credentials → New Credential → Google PaLM API

   - Paste your API key and save## 🔧 How It Works



### Step 3: Notion API SetupThe workflow consists of 4 main components:



1. **Create Integration**:1. **🔗 GitHub Trigger**: Monitors your repository for new or updated issues

   - Go to [Notion Integrations](https://www.notion.com/my-integrations)2. **🤖 AI Agent**: Uses Google Gemini to intelligently summarize and structure issue data

   - Click "New integration"3. **📋 Structured Output Parser**: Formats the AI response into consistent JSON structure

   - Fill in details and enable capabilities:4. **📊 Notion Database**: Creates organized pages with enriched issue information

     - ✅ Read content

     - ✅ Update content  ### Workflow Process:

     - ✅ Insert content1. **Issue Detection** → GitHub webhook triggers when issues are created/updated

   - Copy the Internal Integration Token2. **AI Processing** → Gemini AI analyzes the issue and creates:

   - Concise summary

2. **Create Notion Database**:   - Actionable items

   - Create a new database in Notion   - Additional context notes

   - Add the columns as specified in the table above3. **Data Structuring** → Output is formatted with repository metadata

   - Share the database with your integration4. **Notion Creation** → Structured data becomes a new Notion database page



3. **Configure n8n Credentials**:## 📊 Notion Database Structure

   - In n8n → Credentials → New Credential → Notion API

   - Paste your integration token and saveThe workflow creates Notion pages with the following properties:



### Step 4: Import and Configure Workflow| Column Name          | Type     | Description                    |

|---------------------|----------|--------------------------------|

1. **Import Workflow**:| **Title**           | Title    | Issue title from GitHub       |

   - Download `Github issue to notion database page.json`| **Summary**         | Text     | AI-generated concise summary  |

   - In n8n → Import from file| **Action Items**    | Text     | Key tasks and next steps      |

   - Select the JSON file| **Notes**           | Text     | Additional context            |

| **Repository**      | Text     | Repository name               |

2. **Configure Nodes**:| **Repository URL**  | URL      | Direct link to repository     |

   - **GitHub Trigger**: Select your credentials and repository| **Status**          | Select   | Issue state (open/closed)     |

   - **Google Gemini Chat Model**: Select your Gemini credentials| **Last Activity**   | Date     | Last update timestamp         |

   - **Notion Node**: Select your credentials and target database| **Assigned To**     | Text     | GitHub assignee information   |



3. **Activate Workflow**:## Set up steps

   - Test the workflow with a sample issue- Takes about **10–15 minutes** to set up  

   - Activate for continuous monitoring- You’ll need:

  - A **GitHub token** (for repo access)  

## 🎯 Features  - A **Notion API token** (with database shared)  

  - A **Google Gemini API key**  

- **🤖 AI-Powered Summarization**: Intelligent analysis of issue content- Configure the **GitHub Trigger**, **AI Agent**, and **Notion Database node**  

- **📊 Structured Data**: Consistent formatting for easy tracking- Activate the workflow, and you’re done 🚀  

- **🔄 Real-time Sync**: Automatic updates when issues change

- **🏷️ Rich Metadata**: Repository info, timestamps, and assignee tracking

- **📋 Action Items**: AI-extracted tasks and next steps
- **🔗 Direct Links**: Quick access to original GitHub issues

## 💡 Use Cases

- **Project Management**: Centralize issue tracking across multiple repositories
- **Team Coordination**: Keep stakeholders informed with AI summaries
- **Sprint Planning**: Organized view of issues with action items
- **Progress Tracking**: Monitor issue lifecycle and updates
- **Documentation**: Maintain structured records of development tasks

## 🛠️ Customization

You can customize the workflow by:

- **Modifying AI Prompts**: Adjust the summary style and focus areas
- **Adding Fields**: Include additional GitHub metadata
- **Filtering Issues**: Add conditions to process specific issue types
- **Notification**: Connect to Slack, email, or other services

## 📋 Troubleshooting

**Common Issues:**

1. **GitHub Webhook Not Triggering**:
   - Verify repository permissions
   - Check webhook URL in GitHub settings

2. **Notion Pages Not Created**:
   - Ensure database is shared with integration
   - Verify column names match exactly

3. **AI Responses Inconsistent**:
   - Review and refine the prompt in AI Agent node
   - Check Google Gemini API quota

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

⭐ **Star this repository** if you find it helpful! 

💬 **Questions?** Open an issue or reach out to [AkilLabs](https://github.com/AkilLabs)