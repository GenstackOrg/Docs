# Genstack Python SDK — Method Guide

The Genstack Python SDK offers a powerful and flexible API interface to interact with Genstack's platform. If you're looking for a method not listed here, you can contribute or review the SDK directly on [GitHub](https://github.com/GenstackOrg/Python-SDK).

This guide walks you through all available methods and how to use them effectively.

---

## Installation & Setup

Install the SDK and environment dependency:

```bash
pip install genstack python-dotenv
```

In your `.env` file, set your API key:

```
GENSTACK_API_KEY=<YOUR_API_KEY_HERE>
```

> **Important:** Never expose your API key publicly.

Initialize the SDK client:

```python
import os
from dotenv import load_dotenv
from genstack import Genstack

load_dotenv()

client = Genstack(api_key=os.getenv('GENSTACK_API_KEY'))
```

---

## `client.generate()` — Primary Generation Method

The `generate()` method is the core of the Genstack SDK. All other functionalities revolve around or build upon this.

### Parameters

* `input` *(str)*:
  The unique input prompt or data that you want the model to generate content from. This is required.

* `track` *(str)*:
  The ID of the track you'd like to use. You can find this in your Genstack dashboard at [genstack.fly.dev](https://genstack.fly.dev).

* `model` *(str)*:
  The ID of the model to be used for generation. Although this parameter is currently required, future versions will allow you to configure a default model directly on the Genstack web platform.

### Example Usage

```python
response = client.generate(
    input="Generate a startup pitch for a productivity app",
    track="track_abc123",
    model="model_xyz789"
)

print(response)
```

---

## Contributing

This SDK is fully open-source. If you have suggestions, want to report a bug, or wish to implement a missing method, feel free to open an issue or contribute directly:
[https://github.com/GenstackOrg/Python-SDK](https://github.com/GenstackOrg/Python-SDK)

---

## Summary

* Use `generate()` for all primary generation tasks.
* Ensure your `.env` file securely holds your API key.
* You must provide both a valid `track` ID and a `model` ID.
* Stay updated via the Genstack platform and GitHub repository.

Build faster. Build smarter. Build with Genstack.
