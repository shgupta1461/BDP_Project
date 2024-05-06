# Realtime Sentiment Analysis of YT comments using Spark and Kafka

Group 3:
- Shubham Gupta (202318052)
- Riya Dave (202318011)
- Mayan Bhut (202318043)

## Project Structure
![WhatsApp Image 2024-05-06 at 23 15 37_796fb6da](https://github.com/shgupta1461/BDP_Project/assets/64950073/2ca34ea6-57ac-427b-a44b-e775f3d34a1d)

## How it works
1. The Web App starts the CommentsProvider, WebServer and the Sentiment Analysis Consumer each on a different Thread.
2. The CommentsProvider starts the YoutubeScraper that fetches videos using a Search Term then monitors the videos.
3. The Spark App loads the trained pickled models, starts a Kafka Consumer that listens to incoming comments, performs sentiment analysis then sends the results using a Kafka Producer (The WebApp will then send the results to clients connected in the WebServer).
4. The HTML app connects to the WebServer, listens to incoming results and shows them in the page (it will also fetch the video's title if needed).

## Testing
1. Start the Kafka Zookeeper and Server.
2. Start the web_app.py.
3. Open the index.html in the browser.
4. Start the sentiment_analysis.py (using SparkSubmit).
5. Wait for the analysis to show in the page..
