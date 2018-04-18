# moodbot

moodbot/ 

├── data/

│   ├── stories.md            # dialogue training data

│   └── nlu.md                # nlu training data

├── domain.yml                # dialogue configuration

└── nlu_model_config.json     # nlu configuration


#### Train NLU Model
- `python -m rasa_nlu.train -c nlu_model_config.json --fixed_model_name current`

#### Train Dialogue Model

- `python -m rasa_core.train -s data/stories.md -d domain.yml -o models/dialogue --epochs 300`


#### Run Bot CLI

- `python -m rasa_core.run -d models/dialogue -u models/nlu/default/current`

#### Run Bot Server

- `python -m rasa_core.server -d models/dialogue -u models/nlu/default/current -o out.log`

-d, which is the path to the Rasa Core model.

-u, which is the path to the Rasa NLU model.

-o, which is the path to the log file.

#### Parse Request to Bot

` curl -XPOST localhost:5005/conversations/default/parse -d '{"query":"hello there"}'`