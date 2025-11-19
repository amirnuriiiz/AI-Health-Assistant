# AI Mental Health Companion

Final project for the Building AI course

## Summary

This project develops an AI-powered chatbot that provides mental health support through conversational AI. It uses NLP to understand user emotions and offers resources, coping strategies, and referrals to professionals. About 250 characters.

## Background

Mental health issues are prevalent globally, with depression and anxiety affecting millions. Many people lack access to immediate support due to cost, stigma, or availability. My motivation comes from witnessing friends struggle to find timely help. This project is important because AI can provide accessible, 24/7 support to bridge gaps in mental health care.

* Problem 1: High cost of therapy sessions.
* Problem 2: Long waiting times for professional help.
* Problem 3: Social stigma preventing people from seeking help.

## How is it used?

Users interact with the chatbot via a web or mobile app. They can describe their feelings, and the AI responds with empathetic messages, evidence-based techniques (e.g., CBT exercises), and suggests resources like hotlines or therapists. It is used in private settings whenever someone needs emotional support.

![Mental Health Image](https://images.unsplash.com/photo-1559757148-5c350d0d3c56?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60) *Note: This image is from Unsplash and is free to use under the Unsplash License.*

Example code for sentiment analysis:

```python
from textblob import TextBlob

def analyze_sentiment(text):
    analysis = TextBlob(text)
    polarity = analysis.sentiment.polarity
    if polarity > 0:
        return "positive"
    elif polarity == 0:
        return "neutral"
    else:
        return "negative"

# Example usage
user_input = "I feel really anxious today."
sentiment = analyze_sentiment(user_input)
print(f"The sentiment is {sentiment}.")
