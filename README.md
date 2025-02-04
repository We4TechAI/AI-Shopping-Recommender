# AI Shopping Recommender 🛍️


![AI Shopping Recommender](banner.png)


An intelligent shopping assistant that combines product search with AI-powered analysis to help users make informed purchasing decisions. The application leverages SerpAPI for product search and Groq's LLM for detailed product analysis and personalized recommendations.

## 🌟 Features

- **Smart Product Search**: Search products across multiple stores with location-based results
- **AI-Powered Analysis**: Get personalized product recommendations based on your preferences
- **Beautiful UI**: Clean, modern interface with responsive design
- **Location-Based Results**: Get relevant product listings based on your location
- **Detailed Comparisons**: AI-generated analysis of features, prices, and value propositions

## 🚀 Quick Start

### Using Docker

```bash
# Clone the repository
git clone https://github.com/We4TechAI/AI-Shopping-Recommender.git
cd AI-Shopping-Recommender

# Build Docker image
docker build --tag ai_shopping_recommender:latest .

# Run container
docker run -d --name ai_shopping_recommender -p 8501:8501 ai_shopping_recommender:latest
```

### Manual Installation

1. Clone the repository:
```bash
git clone https://github.com/We4TechAI/AI-Shopping-Recommender.git
cd AI-Shopping-Recommender
```

2. Create and activate virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
Create a `.env` file in the project root with:
```env
SERPAPI_KEY=your_serpapi_key
GROQ=your_groq_api_key
```

5. Run the application:
```bash
streamlit run app.py
```

## 📦 Dependencies

- Python 3.8+
- Streamlit
- SerpAPI
- Groq
- python-dotenv
- pandas


## 💻 Usage

1. Open your browser and navigate to `http://localhost:8501`
2. Enter the product you're looking for
3. Specify your location for relevant results
4. Enter your preferences (budget, features, brand preferences, etc.)
5. Click "Search and Analyze" to get personalized recommendations

## 🔧 Configuration

The application can be configured through environment variables:

| Variable | Description | Required |
|----------|-------------|----------|
| SERPAPI_KEY | Your SerpAPI API key | Yes |
| GROQ | Your Groq API key | Yes |

## 📝 API Documentation

### SerpAPI Integration
The application uses SerpAPI's Google Shopping search with the following parameters:
- `engine`: google_shopping
- `google_domain`: google.com
- `hl`: hi (Hindi language support)
- `gl`: in (India region)
- Location-based searching

### Groq Integration
Uses Groq's LLM (llama-3.3-70b-versatile) for:
- Product analysis
- Feature comparison
- Personalized recommendations
- Price analysis

## 🛠️ Development

### Project Structure
```
AI-Shopping-Recommender/
├── main.py
├── Dockerfile
├── requirements.txt
├── .env.example
├── .env
└── README.md
 
```

### Adding New Features

1. Create a new branch:
```bash
git checkout -b feature/your-feature-name
```

2. Make your changes
3. Test thoroughly
4. Submit a pull request

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details

## 🔐 Security

- Never commit your `.env` file
- Keep API keys secure
- Regularly update dependencies
- Follow security best practices

## 🐛 Troubleshooting

### Common Issues

1. **API Key Issues**
   - Ensure your API keys are correctly set in `.env`
   - Verify API key permissions

2. **Docker Issues**
   - Ensure ports are not in use
   - Check Docker logs: `docker logs ai_shopping_recommender`

3. **Search Issues**
   - Verify internet connection
   - Check SerpAPI quota
   - Ensure location format is correct

## 📞 Support

For support, please:
1. Check existing issues
2. Create a new issue with detailed information
3. Join our community discussions

## ✨ Acknowledgments

- SerpAPI for product search capabilities
- Groq for AI analysis
- Streamlit for the web framework
- All contributors who have helped shape this project

---

Made with ❤️ by We4TechAI Team
