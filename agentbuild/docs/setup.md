#
> Pattern AI agent is a versatile, voice enabled agent designed to enhance and streamline how users converse with digital services across multiple domains. These interactions remain human-like, with tightly tailored responses that allow the agent to serve as a true partner in meeting users needs and requests.
## Installation Guide {: .title}
Follow these steps to set up and run the project using Poetry.
#### 1. Clone the Repository {: .sub-heading}

```bash
git clone https://github.com/PatternAILabs/patternai-agent-build.git
cd patternai-agent-build
```

#### 2. Install Poetry (if not already installed) {: .sub-heading}

**For macOS/Linux:**
```bash
curl -sSL https://install.python-poetry.org | python3 -
```

**For Windows (using PowerShell):**
```powershell
(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | python -
```

#### 3. Configure Poetry for In-Project Virtual Environments {: .sub-heading}

```bash
poetry config virtualenvs.in-project true
```

#### 4. Initialize and Install Dependencies {: .sub-heading}

```bash
poetry install
```

#### 5. Activate the Virtual Environment {: .sub-heading}

**For macOS/Linux:**
```bash
source $(poetry env info --path)/bin/activate
```

**For Windows:**
```cmd
.venv\Scripts\activate
```

#### 6. Set Up Environment Variables {: .sub-heading}

Create a `.env` file in the project root with the following variables:

```bash
# AI Service APIs
OPENROUTER_API_KEY=your_openrouter_key
OPENAI_API_KEY=your_openai_key_here
ELEVENLABS_API_KEY=your_elevenlabs_key

# Google Cloud Credentials (JSON format)
GOOGLE_APPLICATION_CREDENTIALS={"type": "service_account", "project_id": "your-project-id", ...}

# Langfuse Configuration
LANGFUSE_SECRET_KEY=your_langfuse_secret_key
LANGFUSE_PUBLIC_KEY=your_langfuse_public_key
LANGFUSE_HOST=https://cloud.langfuse.com

# WhatsApp Business API
WHATSAPP_ACCESS_TOKEN=your_whatsapp_access_token
DEMO_PHONE_NUMBER_ID=your_phone_number_id
DEMO_BUSINESS_ACCOUNT_ID=your_business_account_id
META_VERIFY_TOKEN=verify_token

# Database Configuration
POSTGRES_HOST
POSTGRES_PORT
POSTGRES_USER
POSTGRES_PASSWORD=your_postgres_password
POSTGRES_DB=whatsapp

# Redis Configuration
REDIS_HOST
REDIS_PORT
REDIS_DB
REDIS_USERNAME=your_redis_username
REDIS_PASSWORD=your_redis_password

# Test Configuration
TEST_PHONE_NUMBER
```

### Running the Application {: .sub-heading}

PatternAI Agent can be run in different modes depending on your needs:

#### Method 1: Using VS Code Launch Configurations (Recommended) {: .sub-heading}

The project includes pre-configured launch settings for VS Code that make development easier:

1. Open the "Run and Debug" sidebar (Ctrl+Shift+D or Cmd+Shift+D)
2. Select the desired configuration from the dropdown:

     - **Launch Demo UI** - Starts Streamlit interface
     - **Launch API Server** - Starts backend API
     - **Launch UI + API** - Starts both components

3. Click the green play button or press F5

#### Method 2: Command Line Execution {: .sub-heading}

**Run both UI+API**

```bash
# Terminal 1: Start API Server
poetry run python -m clients.demo.server --local

# Terminal 2: Start Demo UI
poetry run streamlit run clients/demo/app.py
```

### Development Tools {: .sub-heading}

The following development tools are configured in the Poetry environment to ensure high code quality, maintainability, and productivity.

| Tool | Command | Purpose |
|------|---------|---------|
| Type Checking | `poetry run mypy .` | Static type analysis |
| Linting | `poetry run ruff check .` | Code quality checks |
| Testing | `poetry run pytest` | Run unit & integration tests |

#### Managing Dependencies {: .sub-heading}

##### Adding Dependencies

**Add a new package:**
```bash
poetry add package-name
```

**To add a package with specific version:**
```bash
poetry add "package-name>=1.0.0"
```

##### Removing Dependencies
**To remove a package:**
```bash
poetry remove package-name
```

##### Updating Dependencies

**To update all dependencies:**
```bash
poetry update
```

**To update a specific package:**
```bash
poetry update package-name
```
<br>
!!! info "PatternAI Starter Pack"
    **Quick take on — [User documentation](/user/)**  
    **Peek into the system — [Developer documentation](/developer/)**
<br>
<br>
