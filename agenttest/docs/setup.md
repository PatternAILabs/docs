#
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
LLM_MODEL= model_used
# Langfuse Configuration
LANGFUSE_SECRET_KEY=your_langfuse_secret_key
LANGFUSE_PUBLIC_KEY=your_langfuse_public_key
LANGFUSE_HOST=https://cloud.langfuse.com
```

### Running the Application {: .sub-heading}

PatternAI Agenttest can be run using the command :
```bash
poetry run streamlit run app.py
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
