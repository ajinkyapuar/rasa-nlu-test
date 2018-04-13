# Rasa-NLU-test

- `docker-compose up`

- Train
    - `curl -X POST -d "@./my-data.json" "localhost:5000/train?name=rasaTutorialBot"`
    
- Parse
    - `curl --request POST \
      --url http://localhost:5000/parse \
      --header 'content-type: application/json' \
      --data '{
     "q": "I want to hear a chuck norris joke about school",
     "model": "rasaTutorialBot"
    }' | python -mjson.tool
    `