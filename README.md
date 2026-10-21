Local GGUF AI with llama.cpp 🚀

This project demonstrates how to run a local AI language model using "llama.cpp" and a ".gguf" model file on Windows.

🛠️ Technologies

- llama.cpp
- GGUF language models
- Windows Command Prompt
- Local AI inference server

▶️ Run the Model

llama-server.exe -m "name.gguf" -c 4096 -t 8 --host 127.0.0.1 --port 8080 --dry-penalty-last-n 64

Replace "name.gguf" with the filename or path of your downloaded GGUF model.

Once the server starts, open:

http://127.0.0.1:8080

✨ Features

- Run AI models locally.
- Use GGUF model files.
- Access the model through a local web interface.
- Experiment with local AI without requiring a cloud AI API for inference.

📌 Notes

Performance depends on your model, hardware, and configuration.

This repository shares the demonstration and setup instructions. Model files are not included.

👨‍💻 Author

Created as a personal local AI experiment.

If you find this project useful, consider giving the repository a ⭐.