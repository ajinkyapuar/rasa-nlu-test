# tutorial

- `docker-compose up`

- Train
    - `curl -X POST -d "@./data/testData.json" "localhost:5000/train?name=rasaTutorialBot"`
    
- Status
    - `curl -X GET localhost:5000/status | python -mjson.tool`
    
- Parse
    - `curl --request POST \
      --url http://localhost:5000/parse \
      --header 'content-type: application/json' \
      --data '{
     "q": "What services do you guys provide?",
     "model": "rasaTutorialBot"
    }' | python -mjson.tool`