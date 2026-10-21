⚡ Local GGUF AI with llama.cpp

<p align="center">
  <strong>Run AI models locally on your own Windows PC.</strong>
  <br />
  Private • Lightweight • Developer-Friendly
</p><p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="Windows" />
  <img src="https://img.shields.io/badge/Engine-llama.cpp-00A67D?style=for-the-badge" alt="llama.cpp" />
  <img src="https://img.shields.io/badge/Model-GGUF-8A2BE2?style=for-the-badge" alt="GGUF" />
  <img src="https://img.shields.io/badge/Cost-Free-2EA44F?style=for-the-badge" alt="Free" />
</p>---

🚀 About the Project

Local GGUF AI with llama.cpp is a simple project that demonstrates how to run a local AI language model using "llama.cpp" and GGUF model files on Windows.

Launch a local AI server, open its interface in your browser, and experiment with AI without needing a cloud-based chatbot service.

Whether you're exploring local AI, learning about language models, or experimenting with AI-powered coding assistants, this project is a great place to start.

✨ Features

- 🖥️ Run AI Locally — Run compatible GGUF models on your own computer.
- 🌐 Browser Access — Open the local server interface in your web browser.
- 🔒 Localhost Binding — The example server listens on your own PC.
- ⚙️ Configurable Settings — Adjust context size, CPU threads, and other options.
- 👨‍💻 Coding Assistant Models — Experiment with code-focused models such as Qwen2.5-Coder.
- 🆓 No API Key Required — The local model can run without a paid AI API.
- 📚 Beginner-Friendly — Learn the basics of running local AI models.

🧰 Requirements

Before getting started, make sure you have:

- A Windows PC.
- A compatible "llama.cpp" Windows build.
- A downloaded ".gguf" model file.
- Enough RAM for your chosen model and context size.
- Basic knowledge of using Command Prompt.

«Note: Performance depends on your hardware, model size, quantization, and context length. Larger context sizes require additional memory.»

📥 Step 1 — Download llama.cpp

Download a compatible prebuilt Windows version of "llama.cpp" from the official releases page:

🔗 "Download llama.cpp Releases" (https://github.com/ggml-org/llama.cpp/releases)

Extract the downloaded archive and locate "llama-server.exe".

For example:

D:\llama.cpp\
├── llama-server.exe
└── models\
    └── model.gguf

Your folder structure may be different. Use the actual paths on your computer.

🤖 Step 2 — Download a GGUF Model

Try this coding-focused model:

Qwen2.5-Coder-1.5B-Instruct-GGUF

🔗 "Download from Hugging Face" (https://huggingface.co/Qwen/Qwen2.5-Coder-1.5B-Instruct-GGUF/tree/main)

This is an instruction-tuned model designed for coding tasks, code generation, and code-related assistance.

Which model file should you choose?

- "Q4_K_M" — A useful starting point for balancing model size and quality.
- Other quantizations may be available depending on the model repository.

Download the ".gguf" file you want and save it somewhere convenient.

«Important: The model must be compatible with your version of "llama.cpp". Check the model repository for available files and usage guidance.»

⚡ Step 3 — Start Your Local AI Server

Open Command Prompt in the folder containing "llama-server.exe".

Run this command, replacing the example model path with the actual path to your downloaded file:

llama-server.exe -m "D:\llama.cpp\models\your-model.gguf" -c 4096 -t 8 --host 127.0.0.1 --port 8080 --dry-penalty-last-n 64

🛠️ What do these options mean?

Option| Description
"-m"| Specifies the GGUF model file
"-c 4096"| Sets the context size to 4,096 tokens
"-t 8"| Uses 8 CPU threads
"--host 127.0.0.1"| Binds the server to your local computer
"--port 8080"| Uses port 8080
"--dry-penalty-last-n 64"| Configures the DRY repetition-penalty window

Tip: Adjust the CPU thread count and context size to suit your hardware. If a command-line option is unsupported by your build, check "llama-server.exe --help".

🌐 Step 4 — Open AI in Your Browser

Once the server starts successfully, open:

👉 http://127.0.0.1:8080

You should be able to access the server's browser interface and interact with your loaded model.

Keep the Command Prompt window open while using the server. Close it when you're finished.

🔐 Privacy & Network Notes

This example binds the server to "127.0.0.1", making it accessible through your own computer's loopback interface.

- Your prompts are sent to the local server.
- Running an already-downloaded model does not inherently require an AI API key.
- Downloading the model and any required software still requires an internet connection.
- Local execution does not automatically guarantee that every component is offline or that no network activity occurs.
- Avoid exposing the server to a public network unless you understand the security implications.

🧪 Troubleshooting

<details>
<summary><strong>❌ Model file not found</strong></summary>Check the path after "-m". Make sure the filename and ".gguf" extension are correct.

</details><details>
<summary><strong>❌ Not enough memory</strong></summary>Try a smaller model, a more compact quantization, or a lower context size.

</details><details>
<summary><strong>❌ Browser page does not open</strong></summary>Confirm that the server started without errors and that port "8080" is available. Keep the server running while opening the page.

</details><details>
<summary><strong>❌ Unknown command-line argument</strong></summary>Run "llama-server.exe --help" and verify that your build supports the argument you used.

</details>📸 Screenshots & Demo

Want to see it in action?

Add screenshots or a link to your demonstration video here.

screenshots/
├── terminal.png
└── browser-ui.png

Replace this example section with your own screenshots or video link when available.

🔗 Useful Resources

- 🦙 "llama.cpp — Official Repository" (https://github.com/ggml-org/llama.cpp)
- 🤗 "Qwen2.5-Coder-1.5B-Instruct-GGUF" (https://huggingface.co/Qwen/Qwen2.5-Coder-1.5B-Instruct-GGUF/tree/main)
- 📖 "Qwen2.5-Coder Model Information" (https://huggingface.co/Qwen/Qwen2.5-Coder-1.5B-Instruct-GGUF)
- 💻 "llama.cpp Releases" (https://github.com/ggml-org/llama.cpp/releases)

🤝 Contributing

Suggestions, improvements, and beginner-friendly guides are welcome!

1. Fork this repository.
2. Create a branch for your changes.
3. Submit a pull request describing your improvements.

📄 License

This repository provides instructions and example commands for running local AI models. Unless otherwise specified, the model weights and the software used here are governed by their respective licenses.

Check the relevant project licenses before redistributing software or model files.

---

<p align="center">
  <strong>⚡ Explore Local AI. Learn by Building. Run It Yourself.</strong>
  <br />
  Made for local AI enthusiasts and developers.
</p>.