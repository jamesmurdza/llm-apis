## OpenAI

🔑 Get API key [here](https://platform.openai.com/account/api-keys).

### Chat
```bash
curl "https://api.openai.com/v1/chat/completions" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer $OPENAI_API_KEY" \
  -d '{
    "model": "gpt-3.5-turbo",
    "messages": [
      {
        "role": "system",
        "content": "You are a helpful assistant."
      },
      {
        "role": "user",
        "content": "Hello!"
      }
    ]
  }'
```

### Embeddings
```bash
curl "https://api.openai.com/v1/embeddings" \
  -H "Authorization: Bearer $OPENAI_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "input": "The food was delicious and the waiter...",
    "model": "text-embedding-ada-002",
    "encoding_format": "float"
  }'
```

## Mistral

🔑 Get API key [here](https://console.mistral.ai/users/api-keys/).

### Chat
```bash
curl "https://api.mistral.ai/v1/chat/completions" \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H "Authorization: Bearer $MISTRAL_API_KEY" \
  -d '{
    "model": "mistral-tiny",
    "messages": [{"role": "user", "content": "Who is the most renowned French painter?"}]
  }'
```

### Embeddings
```bash
curl "https://api.mistral.ai/v1/embeddings" \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H "Authorization: Bearer $MISTRAL_API_KEY" \
  -d '{
    "model": "mistral-embed",
    "input": ["Embed this sentence.", "As well as this one."]
  }'
```

## Google

🔑 Get API key [here](https://makersuite.google.com/app/apikey).

### Chat
```bash
curl "https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent?key=$GOOGLE_API_KEY" \
  -H 'Content-Type: application/json' \
  -X POST \
  -d '{
    "contents": [
      {
        "parts": [
          {
            "text": "Write a story about a magic backpack."
          }
        ]
      }
    ]
  }'
```

### Embeddings
```bash
curl "https://generativelanguage.googleapis.com/v1beta/models/embedding-001:generateContent?key=$GOOGLE_API_KEY" \
  -H 'Content-Type: application/json' \
  -X POST \
  -d '{
    "contents": [
      {
        "parts": [
          {
            "text": "This is a sentence."
          }
        ]
      }
    ]
  }'
```
