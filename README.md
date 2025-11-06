# Ctrl+Alt+Heal: Preventive Healthcare Chatbot 🏥

A intelligent preventive healthcare chatbot built with IBM watsonx Agent Lab as part of the IBM SkillsBuild program. This AI-powered health assistant helps users stay healthy through personalized wellness guidance, health education, and evidence-based recommendations.

## 📋 Overview

This chatbot leverages IBM watsonx.ai's advanced AI capabilities to provide comprehensive preventive healthcare information. It combines the power of large language models with external knowledge sources to deliver accurate, contextual health guidance while maintaining a supportive and educational approach.

**Key Features:**
- 🤖 Powered by Meta Llama 3.3 70B Instruct model via IBM watsonx.ai
- 📚 RAG (Retrieval-Augmented Generation) integration with healthcare datasets
- 🔍 Real-time information retrieval via Google Search and Wikipedia
- 💬 Conversational AI interface with memory persistence
- 🌍 Multilingual and accessibility-focused design
- 🔒 Privacy-preserving interactions

## 🎯 Use Cases

The chatbot provides guidance on:
- Healthy lifestyle habits and wellness routines
- Routine health screenings and vaccinations
- Nutrition and dietary recommendations
- Physical activity and exercise guidance
- Stress management techniques
- Sleep hygiene and improvement
- Early detection and preventive care
- Age-specific health considerations

**Important:** This chatbot is designed for educational and informational purposes only. It is NOT a substitute for professional medical advice, diagnosis, or treatment. Always consult healthcare providers for specific medical concerns.

## 🏗️ Architecture

### Technology Stack

- **AI Foundation:** IBM watsonx.ai
- **Language Model:** Meta Llama 3.3 70B Instruct
- **Framework:** LangGraph with LangChain
- **Agent Type:** ReAct (Reasoning + Acting) agent
- **Memory:** Persistent conversation memory with MemorySaver
- **Programming Language:** Python 3.11+

### Integrated Tools

1. **RAG Query Tool**
   - Searches healthcare documents and datasets
   - Provides grounded answers based on uploaded knowledge base
   - Connected to Kaggle healthcare datasets

2. **Google Search**
   - Real-time web search for current health information
   - Access to latest medical research and guidelines

3. **Wikipedia**
   - Access to comprehensive medical and health encyclopedia
   - Configurable to return top 5 most relevant results

### Agent Workflow

```
User Query → Agent Router → Tool Selection → Information Retrieval → Response Generation → User
                ↑                                                                              |
                |                                                                              |
                └──────────────────── Conversation Memory ←────────────────────────────────────┘
```

## 🚀 Getting Started

### Prerequisites

- Python 3.11 or higher
- IBM Cloud account with watsonx.ai access
- IBM Cloud API key
- Access to IBM watsonx.ai project or space

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/kaitlin12210/healthcare-chatbot.git
   cd healthcare-chatbot
   ```

2. **Install required dependencies**
   ```bash
   pip install langgraph
   pip install langchain-ibm
   pip install matplotlib-venn
   pip install ibm-watsonx-ai
   pip install langchain-core
   ```

3. **Set up IBM watsonx credentials**
   - Obtain your IBM Cloud API key from [IBM Cloud Console](https://cloud.ibm.com/docs/account?topic=account-userapikey&interface=ui)
   - You'll be prompted to enter it when running the notebook

### Running the Chatbot

1. Open the Jupyter notebook:
   ```bash
   jupyter notebook Ctrl+Alt+Heal_Preventive_Healthcare_Chatbot.ipynb
   ```

2. Execute cells sequentially to:
   - Import dependencies
   - Configure watsonx API connection
   - Set up the model and parameters
   - Create the agent with integrated tools
   - Start the interactive chatbot

3. When prompted, enter your health-related question and receive personalized guidance!

## ⚙️ Configuration

### Model Parameters

```python
model_id = "meta-llama/llama-3-3-70b-instruct"

parameters = {
    "frequency_penalty": 0,      # Reduces repetition
    "max_tokens": 2000,          # Maximum response length
    "presence_penalty": 0,        # Encourages topic diversity
    "temperature": 0,             # Deterministic responses (0 = factual)
    "top_p": 1                    # Nucleus sampling threshold
}
```

### System Instructions

The agent is configured as a **Preventative Healthcare Health Assistant** with:
- Evidence-based recommendations from reputable health organizations
- Supportive, friendly, and non-judgmental tone
- Clear disclaimers about medical advice limitations
- Personalized responses based on user context
- Multi-step reasoning capabilities for complex queries

## 📊 Example Interactions

**Example 1: Nutrition Guidance**
```
User: What are some heart-healthy foods I should include in my diet?
Agent: [Searches healthcare datasets and provides evidence-based nutrition recommendations]
```

**Example 2: Preventive Screenings**
```
User: What health screenings should a 35-year-old woman get?
Agent: [Retrieves age-specific screening guidelines from knowledge base]
```

**Example 3: Lifestyle Habits**
```
User: How can I improve my sleep quality?
Agent: [Provides sleep hygiene recommendations with actionable tips]
```

## 🔧 Project Structure

```
healthcare-chatbot/
├── Ctrl+Alt+Heal_Preventive_Healthcare_Chatbot.ipynb  # Main notebook
├── README.md                                           # Project documentation
└── [Healthcare datasets/PDFs]                          # Knowledge base (if applicable)
```

## 🎓 IBM SkillsBuild Program

This project was developed as part of the **IBM SkillsBuild** program, a university student-focused initiative that provides hands-on experience with enterprise AI technologies. The program offers:
- Access to IBM watsonx.ai platform
- Training on AI/ML concepts and tools
- Real-world project experience
- Industry-recognized skills development

## 🔐 Security & Privacy

- API keys are securely handled using `getpass` for credential input
- No personal health information is stored or logged
- All interactions are processed through secure IBM Cloud infrastructure
- Conversation memory is session-based and not persisted long-term

## 📝 License

Licensed Materials - Copyright © 2024 IBM. This project and its source code are released under the terms of the ILAN License.

This notebook is subject to the International License Agreement for Non-Warranted Programs and License Information document for watsonx.ai Auto-generated Notebook. See [License Terms](https://www14.software.ibm.com/cgi-bin/weblap/lap.pl?li_formnum=L-AMCU-BYC7LF) for details.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/kaitlin12210/healthcare-chatbot/issues).

## 👤 Author

**Kaitlin Moore**
- GitHub: [@kaitlin12210](https://github.com/kaitlin12210)
- Project: IBM SkillsBuild Participant

## 🙏 Acknowledgments

- IBM watsonx.ai team for the Agent Lab platform
- IBM SkillsBuild program for educational resources
- Meta for the Llama 3.3 70B Instruct model
- LangChain and LangGraph communities

## 📚 Additional Resources

- [IBM watsonx.ai Documentation](https://www.ibm.com/docs/en/watsonx-as-a-service)
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [IBM SkillsBuild Program](https://skillsbuild.org/)
- [Preventive Healthcare Guidelines (CDC)](https://www.cdc.gov/prevention/)

---

**Disclaimer:** This chatbot provides general health information for educational purposes only. It does not provide medical advice, diagnosis, or treatment. Always seek the advice of your physician or other qualified health provider with any questions you may have regarding a medical condition.
