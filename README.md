# TfL Journey Disruption

An [agent skill](https://agentskills.io/home) that plans TfL journeys, checks live line disruptions, and suggests alternatives when the preferred route is affected.

## What it does

When a user needs a London journey plan with disruption awareness, this skill:

- Resolves locations from postcodes, stations, place names, or coordinates
- Plans journeys with TfL's Journey Results API
- Checks line status for the candidate routes
- Warns when the best route is disrupted
- Suggests alternatives when available

## Installation

### As a Claude Code plugin

```shell
/plugin marketplace add diegopetrucci/ai-agents-skills
/plugin install tfl-journey-disruption@diegopetrucci-claude-plugins
```

### As a skill

```bash
npx skills add https://github.com/diegopetrucci/tfl-journey-disruption --skill tfl-journey-disruption
```

## Usage

Trigger the skill when a user wants a TfL journey plan with disruption awareness:

- **Claude Code:** `/tfl-journey-disruption`
- Or say: "plan a TfL route", "check this London journey for disruptions", or "get me to Soho from Stratford and warn me about delays"

The bundled helper script can also be run directly:

```bash
python3 tfl-journey-disruption/scripts/tfl_journey_disruptions.py "940GZZLUSTD" "W1F 9LD" --depart-at 0900
python3 tfl-journey-disruption/scripts/tfl_journey_disruptions.py --from "Stratford" --to "W1F 9LD" --arrive-by 1800
```

## More Skills Like This

Found this skill useful? Browse all my hand-crafted ones in the [AI Agents skills](https://github.com/diegopetrucci/ai-agents-skills) repo.

## License

MIT
