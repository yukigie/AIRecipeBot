# AIRecipeBot

AIRecipeBot is an intelligent recipe suggestion application that uses:
- 📦 Amazon S3 for storing recipe results
- 🔗 Spoonacular API for real-time recipe suggestions
- 🧠 Amazon Bedrock for natural conversational responses
- 🧠 Amazon Q Business for unified retrieval
- 🖥️ HTML Frontend for input-based interaction

## Folder Structure
- `/frontend/` — Simple HTML UI for inputs
- `/lambda/` — AWS Lambda code to fetch recipes and send to S3
- `/data-samples/` — Example result JSONs for uploading to S3

## Getting Started
1. Upload `lambda/spoonacular_fetch.py` as a Lambda function
2. Create S3 bucket: `ai-recipe-bucket` ➝ upload JSON files into `/api_results/`
3. Connect S3 as data source in Amazon Q Business
4. Deploy API Gateway endpoint for live fetching
5. Use `frontend/index.html` to input ingredients

## Notes
- Don’t forget to add CORS headers and permissions!
- Ensure `.env` or config files with secrets are not committed
