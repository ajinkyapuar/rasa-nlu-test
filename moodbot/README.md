# moodbot

moodbot/ 

├── data/

│   ├── stories.md            # dialogue training data

│   └── nlu.md                # nlu training data

├── domain.yml                # dialogue configuration

└── nlu_model_config.json     # nlu configuration


`python -m rasa_nlu.train -c nlu_model_config.json --fixed_model_name current`