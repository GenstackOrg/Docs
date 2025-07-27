# **Genstack Python SDK**


## **Prerequisites**

Before you proceed, make sure you have:

- **Python** installed (version **3.10 or above** is recommended)
- **pip** — Python’s package manager (comes bundled with Python)

## **Check your setup**

To confirm you have Python and pip ready, run these in your terminal:

```
python --version
pip --version
```


If both commands show versions (like `Python 3.11.5`), you're good to go.

---

### (Optional) Use a virtual environment

It’s a good idea to isolate dependencies per project. To create and activate a virtual environment:

#### On macOS/Linux:

```
python -m venv venv
source venv/bin/activate
```

#### On Windows:

```shell
python -m venv venv
venv\Scripts\activate
```

You’ll know it’s active when your terminal prompt starts with `(venv)`.

## **Install dependencies**

Run the following command to install Genstack and its required packages:

```shell
pip install genstack python-dotenv
```

## **Set up environment variables**

Genstack uses environment variables to manage sensitive config like API keys.

Create a `.env` file in your project root and add the following:

```env
GENSTACK_API_KEY=your-api-key-here
```

Replace `your-api-key-here` with your actual API key. This file should **not** be committed to version control (add it to your `.gitignore`).

## **Run your first Genstack response**

Here's a minimal example to make sure everything's wired up right:

```python
#
from genstack import Genstack
from dotenv import load_dotenv
import os

#
load_dotenv()

#
client = Genstack(api_key=os.getenv("GENSTACK_API_KEY"))

#
response = client.generate(input="Are you ready?", model="<MODEL_ID>", track="<YOUR_TRACK_NAME>")

#
print(response)
```

If everything’s set up, you should see a response printed back from the AI. That’s it — you’re in.