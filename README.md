# 🔍 LLM Evaluation Metrics Dashboard

A comprehensive Streamlit web application for evaluating Large Language Model (LLM) responses using multiple evaluation metrics powered by LlamaIndex.

![Dashboard Preview](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LlamaIndex](https://img.shields.io/badge/LlamaIndex-000000?style=for-the-badge&logo=llamaindex&logoColor=white)

## 📊 Features

- **Multiple Evaluation Metrics**: Assess your LLM responses across four key dimensions:
  - **Faithfulness**: Measures if the answer is grounded in the provided context
  - **Answer Relevancy**: Evaluates how well the answer addresses the original question
  - **Correctness**: Compares semantic accuracy against reference answers
  - **Semantic Similarity**: Computes embedding-based similarity with reference answers

- **Interactive Web Interface**: Clean, user-friendly Streamlit dashboard
- **Real-time Evaluation**: Get instant feedback on your LLM responses
- **Detailed Feedback**: Comprehensive explanations for each metric score
- **Export Results**: Download evaluation results as CSV files
- **Flexible Model Selection**: Choose from multiple OpenAI models for evaluation

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- OpenAI API key

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/llm-evaluation-dashboard.git
cd llm-evaluation-dashboard
```

2. Install required dependencies:
```bash
pip install streamlit
pip install llama-index
pip install llama-index-llms-openai
pip install llama-index-embeddings-openai
pip install pandas
```

3. Run the application:
```bash
streamlit run app.py
```

4. Open your browser and navigate to `http://localhost:8501`

## 🔧 Usage

### Basic Evaluation

1. **Configure Settings** (in sidebar):
   - Enter your OpenAI API key
   - Select evaluation model (GPT-4, GPT-4-turbo, etc.)
   - Choose which metrics to evaluate

2. **Input Data**:
   - **Query/Question**: The original question asked
   - **Context**: Retrieved documents or context used for answering
   - **Generated Answer**: The response from your LLM system
   - **Reference Answer**: Expected or ground truth answer

3. **Run Evaluation**: Click "🚀 Evaluate Metrics" to get results

### Example Input

```
Query: "What is the capital of France?"

Context: "France is a country in Western Europe. Paris is the capital and largest city of France, located in the north-central part of the country."

Generated Answer: "The capital of France is Paris."

Reference Answer: "Paris is the capital city of France."
```

## 📈 Evaluation Metrics Explained

### Faithfulness
- **Purpose**: Detect hallucinations and ensure grounding in context
- **Range**: 0.0 - 1.0 (higher is better)
- **Passing Threshold**: Typically > 0.8

### Answer Relevancy
- **Purpose**: Measure how well the answer addresses the question
- **Range**: 0.0 - 1.0 (higher is better)
- **Evaluation**: Uses LLM-as-a-judge approach

### Correctness
- **Purpose**: Assess semantic accuracy compared to reference
- **Range**: 1.0 - 5.0 (higher is better)
- **Method**: LLM-based semantic comparison

### Semantic Similarity
- **Purpose**: Measure embedding-based similarity
- **Range**: 0.0 - 1.0 (higher is better)
- **Method**: Cosine similarity of OpenAI embeddings

## 🛠️ Configuration

### Environment Variables

Create a `.env` file (optional):
```bash
OPENAI_API_KEY=your_openai_api_key_here
```

### Model Options

Supported evaluation models:
- `gpt-4o` (recommended for best accuracy)
- `gpt-4`
- `gpt-4-turbo`

## 📁 Project Structure

```
llm-evaluation-dashboard/
│
├── app.py                 # Main Streamlit application
├── requirements.txt       # Python dependencies
├── README.md             # This file
├── .env.example          # Environment variables template
└── .gitignore           # Git ignore patterns
```

## 🧪 Example Results

The dashboard provides:
- **Visual Metrics Cards**: Quick score overview with color coding
- **Progress Bars**: Visual representation of performance
- **Detailed Feedback**: Comprehensive explanations for each score
- **Summary Table**: Consolidated view of all metrics
- **CSV Export**: Download results for further analysis

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Development Setup

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes
4. Run tests (if applicable)
5. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
6. Push to the branch (`git push origin feature/AmazingFeature`)
7. Open a Pull Request

## 📝 Requirements

```txt
streamlit>=1.28.0
llama-index>=0.8.0
llama-index-llms-openai>=0.1.0
llama-index-embeddings-openai>=0.1.0
pandas>=1.3.0
```

## ⚠️ Important Notes

- **API Costs**: Evaluation uses OpenAI API calls, which incur costs
- **Rate Limits**: Be mindful of OpenAI rate limits when running batch evaluations
- **Security**: Never commit your API keys to version control

## 🐛 Troubleshooting

### Common Issues

1. **"LlamaIndex not installed" error**:
   ```bash
   pip install llama-index llama-index-llms-openai llama-index-embeddings-openai
   ```

2. **API Key errors**:
   - Ensure your OpenAI API key is valid and has sufficient credits
   - Check that the API key has access to the selected model

3. **Import errors**:
   - Verify all dependencies are installed with correct versions
   - Try creating a fresh virtual environment

## 📚 Resources

- [LlamaIndex Documentation](https://docs.llamaindex.ai/)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [OpenAI API Documentation](https://platform.openai.com/docs)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with [LlamaIndex](https://www.llamaindex.ai/) for evaluation capabilities
- Powered by [Streamlit](https://streamlit.io/) for the web interface
- Uses [OpenAI](https://openai.com/) models for LLM-as-a-judge evaluation

## 📧 Contact

For questions or support, please open an issue on GitHub or contact [your-email@example.com].

---

**⭐ If you find this project helpful, please consider giving it a star!**
