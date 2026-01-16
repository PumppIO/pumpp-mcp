# 🎨 Pumpp-MCP: The Visual Cortex for AI Agents

**Pumpp-MCP** is an open-source Model Context Protocol (MCP) server that grants AI Agents (Cursor, Claude Desktop, Windsurf) the ability to autonomously design, generate, and iterate on visual assets.

By bridging the gap between agentic reasoning and **fal.ai’s** ultra-fast inference, Pumpp-MCP allows developers to move from "code-only" generation to full-stack "visual-ready" deployment.

---

## 🚀 Why Pumpp-MCP?

Currently, AI Agents like Cursor can write incredible code but are "blind" to the visual requirements of a modern brand. They leave developers with empty `<img>` tags or generic stock photos.

**Pumpp-MCP solves this by:**

* **Native IDE Integration:** Agents can call `generate_marketing_asset()` directly from your chat sidebar.
* **Agentic Prompt Engineering:** Automatically translates vague agent requests (e.g., *"Make it look premium"*) into high-fidelity fal.ai prompt structures.
* **Brand Consistency:** Injects LoRA weights and style guides into the inference loop so the agent stays on-brand.
* **Speed-First:** Optimized for sub-2s latencies using fal’s inference engine, ensuring the agentic loop isn't broken.

---

## 🛠 Features

* **Instant Asset Injection:** Automatically generates and saves `.png` or `.mp4` assets into your project directory and updates your code's `src` paths.
* **Smart Refinement:** Agents can "iterate" on an image (e.g., *"Make the lighting warmer"*) using fal's Image-to-Image and In-painting capabilities.
* **Contextual Awareness:** The server reads your local CSS/Theme files to ensure generated assets match your UI's color palette.
* **Extensible Architecture:** Support for Flux, Stable Diffusion, and LTX-Video via the fal.ai API.

---

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/FelixWaweru/pumpp-mcp

# Install dependencies
cd pumpp-mcp
npm install

# Configure your fal.ai API Key
export FAL_KEY="your_fal_key_here"

# Start the MCP server
npm run build && npm run start

```

### Adding to Cursor / Claude Desktop

Add the following to your MCP settings configuration:

```json
{
  "mcpServers": {
    "pumpp": {
      "command": "node",
      "args": ["/path/to/pumpp-mcp/build/index.js"],
      "env": {
        "FAL_KEY": "your_fal_key_here"
      }
    }
  }
}

```

---

## 🔬 Research & Roadmap (Grant Focus)

This project is supported by the **fal Research Grant** initiative, focusing on:

1. **Agent-Model Alignment:** Researching how to fine-tune Flux models to follow strict layout constraints requested by LLMs.
2. **Latent Space Consistency:** Developing a standardized "Style-ID" system that agents can pass between different fal models to maintain character/product consistency.
3. **Inference Benchmarking:** Open-sourcing a performance dashboard comparing cost-per-asset for agentic workflows across major providers.

---

## 🤝 Contributing

We are building the future of autonomous design. If you have ideas for better agent-to-image prompting or new MCP tools, please open an issue or PR.

* **Core Engine:** [Pumpp.io](https://www.pumpp.io)
* **Maintainer:** [Felix Waweru](https://github.com/FelixWaweru)

---

### Next Step for you:

Would you like me to draft a **technical white paper summary** or a **Twitter/X announcement thread** to help you build the social proof that fal.ai looks for when awarding grants?
