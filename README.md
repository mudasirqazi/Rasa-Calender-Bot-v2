# Rasa Calendar Bot v2

## Purpose
A conversational AI assistant designed for healthcare appointment and availability management. The bot enables doctors and healthcare professionals to manage appointments, set availability schedules, and retrieve availability information through natural language interactions.

## Operational Flow
1. **User Greeting**: Bot welcomes users and identifies their intent
2. **Intent Recognition**: Processes user requests for appointments or availability management
3. **Form Activation**: Initiates appropriate forms based on user intent
4. **Data Collection**: Gathers required information through slot filling
5. **Validation**: Validates user inputs using custom validation logic
6. **API Integration**: Communicates with external healthcare API for data operations
7. **Response Generation**: Provides confirmation and relevant information to users

## Project Structure
```
rasa_calendar_botv2/
├── actions/                    # Custom actions and API integrations
│   ├── actions.py             # Form validation and submission actions
│   ├── db_handler.py          # MongoDB database operations
│   └── endpoints.py           # External API communication
├── data/                      # Training data
│   ├── nlu.yml               # Natural language understanding examples
│   ├── stories.yml           # Conversation flow stories
│   └── rules.yml             # Conversation rules and form handling
├── config.yml                # Rasa pipeline and policy configuration
├── domain.yml                # Bot domain with intents, slots, and responses
├── endpoints.yml             # Action server and tracker store configuration
└── credentials.yml           # Channel integration credentials
```

## Language
**Python** (Rasa Framework)

## Tools and Technologies
- **Rasa Open Source**: Core conversational AI framework
- **DIET Classifier**: Intent classification and entity extraction
- **TED Policy**: Transformer-based dialogue management
- **Memoization Policy**: Exact story matching for predictable paths
- **Rule Policy**: Rule-based conversation handling
- **Form Validation**: Custom slot validation and data collection
- **MongoDB**: Database for user session management
- **REST API**: Integration with healthcare management system (ikioo.com)
- **Requests Library**: HTTP client for API communications
- **PyMongo**: MongoDB driver for Python
- **Custom Actions**: Server-side business logic implementation
