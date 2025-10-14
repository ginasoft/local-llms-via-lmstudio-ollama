# Running Open LLMs Locally

The [/code](/code/) folder contains code examples.

## Requirements

To run the examples locally you need:

- **LM Studio** or **Ollama** installed and running.
- The **Gemma 3 12B QAT** model **downloaded locally** and loaded in LM Studio/Ollama before running any scripts.
- **Python 3.10+**
- The following libraries installed:
  - [`requests`](https://pypi.org/project/requests/)
  - [`openai`](https://github.com/openai/openai-python)

---

## Setup Instructions

### Download the model

Before running the scripts, make sure you have downloaded the model you plan to use:

- In **LM Studio**:
  1. Open the **“Models”** tab.
  2. Search for **Gemma 3 12B QAT**.
  3. Click **Download** and wait for the model to finish downloading.
  4. Go to the **Developer** or **Advanced** view and make sure the **local server is running** (“Running” status).

- In **Ollama**:
  ```bash
  ollama pull gemma:3-12b-qat
  ollama run gemma:3-12b-qat
  ```

---

### Create and activate a Python virtual environment

It’s recommended to use a **virtual environment (venv)** to isolate dependencies.

#### Windows (PowerShell)
```bash
python -m venv venv
env\Scripts\activate
```

#### macOS / Linux
```bash
python3 -m venv venv
source venv/bin/activate
```

Once activated, you should see `(venv)` at the start of your terminal prompt.

---

### Install dependencies

With the virtual environment activated, install the required packages:

```bash
pip install requests openai
```

---

### Run the code

Now you can run the Python scripts located in the `/code` folder, for example:

```bash
python code/example_request.py
```

Make sure the **local model server** (LM Studio or Ollama) is running while executing the code.