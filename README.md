#DeepSeek R1 Benchmarking with Ollama

📊 Benchmark DeepSeek R1 models using Ollama and evaluate their token generation speed.

This script benchmarks multiple DeepSeek R1 models on different types of prompts (chat, instruction, and question-answer) and saves the results in a structured format.

🚀 Features
Downloads and sets up DeepSeek R1 models (1.5B, 7B, 8B, 14B, 32B, 70B) automatically.
Runs benchmarking on three types of prompts:
Chat
Instruction
Question-Answer
Saves the generated responses in a structured directory format.
Calculates and displays tokens per second (t/s) for each model.
📦 Installation
1️⃣ Install Ollama
Ensure you have Ollama installed. If not, install it with:

sh
Kopyala
Düzenle
curl -fsSL https://ollama.ai/install.sh | sh
Or visit Ollama's official installation guide for other platforms.

2️⃣ Clone the Repository
sh
Kopyala
Düzenle
git clone https://github.com/YOUR_GITHUB_USERNAME/deepseek-benchmark.git
cd deepseek-benchmark
3️⃣ Install Python Dependencies
Make sure you have Python 3.9+ installed. Then install required dependencies:

sh
Kopyala
Düzenle
pip install ollama
▶️ Usage
Run the script to benchmark DeepSeek models:

sh
Kopyala
Düzenle
python benchmark.py
The script will:

Pull the models (if they are not already downloaded).
Run benchmarks on predefined prompts.
Save results in the answers/ directory.
Display performance metrics (tokens per second).
Example output:

bash
Kopyala
Düzenle
Pulling "deepseek-r1:1.5b" if it does not exist...
Pulling "deepseek-r1:7b" if it does not exist...
...

Benchmarking "deepseek-r1:14b" on "chat" prompts... 7.92t/s.
Benchmarking "deepseek-r1:14b" on "instruct" prompts... 5.48t/s.
Benchmarking "deepseek-r1:14b" on "question-answer" prompts... 6.12t/s.

Overall "deepseek-r1:14b" prompts: 6.51t/s.
📂 Results Directory Structure
After running the benchmark, results are stored in answers/ as follows:

python-repl
Kopyala
Düzenle
answers/
│── deepseek-r1-14b/
│   ├── chat/
│   │   ├── 1.txt
│   │   ├── 2.txt
│   ├── instruct/
│   │   ├── 1.txt
│   │   ├── 2.txt
│   ├── question-answer/
│       ├── 1.txt
│       ├── 2.txt
...
Each .txt file contains the model-generated response for the respective prompt.

⚙️ Customization
You can modify the following:

Modify Model List
To add or remove models, edit the MODELS list in benchmark.py:

python
Kopyala
Düzenle
MODELS = [
  'deepseek-r1:1.5b',
  'deepseek-r1:7b',
  'deepseek-r1:14b',  # Modify as needed
]
Modify Prompts
Edit the PROMPTS dictionary to add custom questions:

python
Kopyala
Düzenle
PROMPTS = {
  'custom-category': [
    'Describe the impact of AI on society.',
    'Write a poem about technology and nature.',
  ]
}
🛠 Troubleshooting
1️⃣ Ollama Not Found
If you see an error like command not found: ollama, ensure Ollama is installed and added to your PATH.

2️⃣ Memory Issues
Larger models (e.g., deepseek-r1:70b) require significant RAM and GPU. Consider using a machine with at least 128GB RAM and a powerful GPU.

3️⃣ Slow Performance
If benchmarking takes too long:

Reduce the number of models in the MODELS list.
Use smaller DeepSeek R1 models (1.5B or 7B).
Upgrade to a high-performance CPU/GPU.
🤝 Contributing
Pull requests are welcome! If you have suggestions for improving the benchmarking process or adding new features, feel free to contribute.

Fork the repository
Create a new branch (git checkout -b feature-branch)
Commit your changes (git commit -m "Add new feature")
Push to the branch (git push origin feature-branch)
Open a Pull Request
📜 License
This project is licensed under the MIT License.

⭐ Support & Feedback
If you found this useful, give it a ⭐ on GitHub! If you encounter any issues, feel free to open an issue or reach out.

📩 Contact: ograssezer474@gmail.com
📍 GitHub: https://github.com/sezerogras
