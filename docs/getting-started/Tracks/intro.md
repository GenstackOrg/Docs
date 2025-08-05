# Introduction

**Tracks** are modular units inside a **project** that give you full control over:

* Modalities (input/output types)
* Response formatting
* Model selection via API

No rigid flows. You define the behavior.

---

## How to Build a Track in Genstack

### 1. **Track Name**

Short, descriptive identifier for your track.

### 2. **Track ID**

Auto-generated from the name. Can be manually overridden.

### 3. **Description**

Optional internal note to describe the track’s purpose.

### 4. **Track Type**

Classify the model scope:

* Reasoning
* Standard LLMs
  *Note: This does **not** limit your model options.*

### 5. **Modalities**

Define input and output types.
**Currently supported:** Text → Text

### 6. **Tools**

Enable tool usage within the track:

* Function calling
* Web search (beta)

---

**You define the logic. Genstack handles the infra.**
