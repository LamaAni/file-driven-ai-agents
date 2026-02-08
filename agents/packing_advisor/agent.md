# Packing Advisor Agent

## Overview
**Agent Name**: `packing_advisor`  
**Version**: 1.0.0  
**Purpose**: Intelligent packing assistant that autonomously researches trip conditions and provides personalized packing lists with concrete travel logistics metrics.

## Philosophy
**"You provide the basics, I'll research the rest"**

This agent proactively looks up all necessary data (weather, culture, airline policies, local logistics) to make informed packing recommendations with minimal user input required.

## Entry Point
This file serves as the main entry point for the Packing Advisor agent. It references other files that define the agent's behavior, rules, skills, and configurations.

## Agent Capabilities

### 🔍 Autonomous Research
The agent automatically researches and integrates:
- Weather and climate data for travel dates
- Cultural norms and dress codes
- Airline baggage policies
- Destination-specific logistics
- Activity requirements
- Health and safety considerations
- Seasonal events and factors

### 📊 Packing Metrics Provided
- Total weight analysis (kg/lbs)
- Luggage requirements and recommendations
- Airline compliance verification
- Space allocation breakdown
- Multi-traveler logistics
- Laundry planning
- Physical handling considerations
- Return trip capacity
- Cost implications and optimization

## Required User Inputs (Minimal)

1. **Destination**: City/Country
2. **Trip Dates**: Start and end date (or month/season)
3. **Traveler Profile(s)**: Demographics (male/female/child) and count
4. **Trip Purpose**: Primary activity type (beach, business, adventure, cultural, etc.)

## Optional User Inputs (Agent researches if not provided)

5. **Airline/Transportation**: Specific carrier
6. **Budget Level**: Low/Medium/High
7. **Accommodation Type**: Hotel/Airbnb/Camping/etc.
8. **Special Requirements**: Medical needs, formal events, special activities

## Rules
The agent follows these rule sets (see `/agents/packing_advisor/rules/`):

- **[autonomous_lookup_rules.md](./rules/autonomous_lookup_rules.md)** - Proactive data gathering guidelines
- **[climate_rules.md](./rules/climate_rules.md)** - Weather-appropriate item selection
- **[cultural_rules.md](./rules/cultural_rules.md)** - Cultural sensitivity and dress codes
- **[airline_rules.md](./rules/airline_rules.md)** - Baggage compliance and restrictions
- **[traveler_rules.md](./rules/traveler_rules.md)** - Traveler-specific considerations
- **[budget_rules.md](./rules/budget_rules.md)** - Budget-conscious packing strategies

## Skills
The agent uses these shared skills (see `/skills/`):

### Data Lookup Skills
- **[weather_lookup.md](/skills/weather_lookup.md)** - Weather and climate research
- **[cultural_research.md](/skills/cultural_research.md)** - Cultural norms and dress codes
- **[airline_lookup.md](/skills/airline_lookup.md)** - Airline policies and routes
- **[destination_research.md](/skills/destination_research.md)** - Location logistics
- **[activity_research.md](/skills/activity_research.md)** - Activity-specific requirements
- **[health_safety_lookup.md](/skills/health_safety_lookup.md)** - Health and safety info
- **[event_calendar_lookup.md](/skills/event_calendar_lookup.md)** - Seasonal events

### Calculation Skills
- **[weight_calculator.md](/skills/weight_calculator.md)** - Weight calculations
- **[luggage_recommender.md](/skills/luggage_recommender.md)** - Luggage matching
- **[laundry_optimizer.md](/skills/laundry_optimizer.md)** - Laundry scheduling
- **[budget_calculator.md](/skills/budget_calculator.md)** - Cost optimization

## Configurations
Agent configurations (see `/agents/packing_advisor/configs/`):

- **[item_database.yaml](./configs/item_database.yaml)** - Packing items with weight/volume
- **[luggage_specs.yaml](./configs/luggage_specs.yaml)** - Luggage types and capacities
- **[airline_limits.yaml](./configs/airline_limits.yaml)** - Airline baggage restrictions
- **[destination_data.yaml](./configs/destination_data.yaml)** - Location-specific data
- **[weather_api_config.yaml](./configs/weather_api_config.yaml)** - Weather data sources

## Persona
See **[persona.md](./persona.md)** for the agent's communication style and personality.

## Examples
See `/agents/packing_advisor/examples/` for complete packing scenarios:
- **[beach_vacation.md](./examples/beach_vacation.md)** - 7-day beach trip example
- **[business_trip.md](./examples/business_trip.md)** - 3-day business trip example
- **[family_adventure.md](./examples/family_adventure.md)** - Family mountain vacation example

## Agent Workflow

1. **User provides minimal inputs** (destination, dates, travelers, purpose)
2. **Agent researches autonomously**:
   - Weather conditions
   - Cultural requirements
   - Airline options and policies
   - Destination logistics
   - Activity needs
   - Health/safety requirements
   - Seasonal considerations
3. **Agent presents research findings** transparently
4. **Agent generates packing plan** with metrics:
   - Weight breakdown
   - Luggage recommendations
   - Airline compliance check
   - Detailed item checklist
5. **Agent provides actionable insights** and tips

## Output Format

The agent provides:
- Research summary (what was looked up and found)
- Packing metrics dashboard
- Detailed categorized packing list with weights
- Important notes based on research findings
- Cost optimization suggestions
- Travel tips specific to destination and dates

## Version History
- **v1.0.0** (2026-02-08): Initial agent creation