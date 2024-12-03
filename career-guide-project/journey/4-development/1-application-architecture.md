# Application Architecture

There are two main parts of application:
- Core
- Server

### Core

> A multi-modular architecture with replacable unit modules.

```txtcore/
├── src/
│   ├── models/
│   │  ├── chat/
│   │  │   ├── OpenAI.py
│   │  │   ├── Groq.py
│   │  │   ├── CustomNLP.py
│   │  │   └── __init__.py
│   │  └── skills/
│   │  │   ├── CustomGPTServices.py
│   │  │   ├── AIML.py
│   │  │   ├── HuggingFaceModel.py
│   │  │   └── __init__.py
│   ├── managers/
│   │  ├── ChatManager.py
│   │  ├── SuccessScoreManager.py
│   │  └── SkillsRecommendationManager.py
│   ├── workers/
│   │  ├── chat_worker.py
│   │  ├── success_score_worker.py
│   │  └── skills_recommendation_worker.py
│   ├── util/
│   │  ├── classes/
│   │  │   ├── TTS.py
│   │  │   ├── STT.py
│   │  │   ├── Vision.py
│   │  │   ├── Database2JSON.py
│   │  │   ├── JSON2Database.py
│   │  │   └── __init__.py
│   │  └── functions/
│   │  │   ├── system_call.py
│   │  │   ├── json_request.py
│   │  │   ├── read_file.py
│   │  │   └── __init__.py
│   ├── dist/
│   │  ├── pretrained_models/
│   │  │   ├── YoloV8.pt
│   │  │   ├── custom_model.weights
│   │  │   ├── aiml_skills.brn
│   │  │   └── __init__.py
│   │  ├── career_categories.json
│   │  └── models.json
│   ├── config/
│   │  ├── settings.py.py
│   │  └── database_connection.py
│   ├── .env
│   └── main.py
├── examples/
├── tests/
└── docs/

```

Skillset:
- Python
- Database

### Server

> Runs `core` models. Manages database, jobs and requests.

```txt
server/
├── src/
│   ├── config/
│   ├── controllers/
│   ├── models/
│   ├── jobs/
│   ├── database/
│   │   ├── migrations/
│   │   └── seeders/
│   ├── views/
│   ├── public/
│   ├── routes/
│   └── .env
└── docs/

```

Platform:
- `Laravel` -- Recommended
- `Node` / `Express` -- Second Recommended
- `Django`
- `Flask`

Database Options:
- `Neo4J` - Recommended
- `MongoDB` - Second Recommended
- `MySQL`
