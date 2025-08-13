# Math Question Generator 🧮

An AI-powered tool for generating similar math questions based on base examples, with LaTeX support and automatic diagram generation.

## 🌟 Features

- **AI-Powered Generation**: Uses OpenAI GPT-4 to create similar questions based on examples
- **LaTeX Support**: Preserves mathematical formulas and equations in LaTeX format
- **Automatic Diagrams**: Generates geometry diagrams using matplotlib
- **Curriculum Aligned**: Maps questions to specific subjects, units, and topics
- **Multiple Export Formats**: Creates Word documents and text files
- **Demo Mode**: Works without API key for testing

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/math-question-generator.git
cd math-question-generator
```

2. **Create virtual environment** (recommended)
```bash
python -m venv venv

# Activate virtual environment
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

### Basic Usage

#### Demo Mode (No API Key Required)
```bash
python generate_questions.py
# Choose option 1 when prompted
```

#### With OpenAI API
```bash
python generate_questions.py
# Choose option 2 and enter your API key when prompted
```

### Python Script Usage
```python
from generator import MathQuestionGenerator

# Initialize generator
generator = MathQuestionGenerator(use_openai=False)  # Demo mode

# Generate questions
questions = generator.generate_questions_manually()

# Create Word document
doc_path = generator.create_word_document(questions)
print(f"Document created: {doc_path}")
```

## 📁 Project Structure

```
math-question-generator/
├── generate_questions.py     # Main script
├── requirements.txt          # Python dependencies
├── README.md                 # This file
├── output/                   # Generated files
│   ├── *.docx               # Word documents
│   ├── *.txt                # Text files
│   └── *.png                # Diagram images
└── base_questions/          # Base question examples
    └── examples.json
```

## 📋 Output Format

Questions are generated in the following format:

```
@title Assessment title
@description Assessment description
@question Question text here
@instruction Instructions for student
@difficulty easy/moderate/hard
@Order Question number
@option First option
@option Second option
@@option Correct answer (marked with @@)
@option Fourth option
@option Fifth option
@explanation Detailed explanation
@subject Quantitative Math
@unit Data Analysis & Probability
@topic Counting & Arrangement Problems
@plusmarks 1
```

## 🎯 Example Questions Generated

### Question 1: Combinations
- **Type**: Counting principles
- **Context**: School lunch combinations
- **Skills**: Multiplication principle

### Question 2: Geometry
- **Type**: Spatial reasoning
- **Context**: Cylinder packing
- **Skills**: Volume and dimensions

## 🛠️ Configuration

### Using OpenAI API

1. Get API key from [OpenAI Platform](https://platform.openai.com)
2. Set in environment variable:
```bash
export OPENAI_API_KEY="your-key-here"
```
Or enter when prompted by the script

### Customizing Questions

Edit the `generate_questions_manually()` function in `generate_questions.py` to modify:
- Question content
- Difficulty levels
- Number of options
- Curriculum mapping

## 📦 Requirements

```txt
openai==1.12.0
python-docx==1.1.0
matplotlib==3.7.1
numpy==1.24.3
python-dotenv==1.0.0
```

## 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| ModuleNotFoundError | Run `pip install -r requirements.txt` |
| API Key Error | Check your OpenAI API key is valid |
| Permission Denied | Run from a folder with write permissions |
| No module named 'pip' | Run `python -m ensurepip --upgrade` |

## 📊 Curriculum Topics Supported

- **Quantitative Math**
  - Problem Solving
  - Algebra
  - Geometry and Measurement
  - Numbers and Operations
  - Data Analysis & Probability
  - Reasoning

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Your Name** - *Initial work* - [YOUR_USERNAME](https://github.com/YOUR_USERNAME)

## 🙏 Acknowledgments

- OpenAI for GPT-4 API
- Math educators for curriculum structure
- Contributors and testers

## 📧 Support

For support, email your.email@example.com or create an [issue](https://github.com/YOUR_USERNAME/math-question-generator/issues).

## 🔮 Future Enhancements

- [ ] Web interface using Flask/Streamlit
- [ ] Support for more question types
- [ ] Image recognition for base questions
- [ ] Batch processing capabilities
- [ ] Export to Google Docs API
- [ ] Question difficulty analysis
- [ ] Student performance tracking

---

**Note**: This tool is designed for educational purposes. Ensure generated questions are reviewed before use in actual assessments.

Made with ❤️ for math educators