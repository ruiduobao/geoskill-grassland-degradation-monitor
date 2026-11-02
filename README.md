# geoskill-grassland-degradation-monitor

> Monitor grassland degradation and recovery trends from multi-temporal vegetation cover, phenology, bare ground and climate baselines. Outputs management zones for restoration prioritization. Use when assessing grassland health, identifying degraded areas, evaluating restoration effectiveness, or generating management recommendations.

See [SKILL.md](SKILL.md) for full usage, inputs and outputs.

## Quick start

```bash
# Basic analysis with default parameters (10 years, Theil-Sen, climate normalized)
python scripts/grassland_degradation_monitor.py --output-dir ./gdm-output

# Custom years and trend method
python scripts/grassland_degradation_monitor.py \
  --years 15 \
  --trend-method ols \
  --output-dir ./gdm-output

# Without climate normalization (raw trend only)
python scripts/grassland_degradation_monitor.py \
  --years 10 \
  --no-climate-normalize \
  --output-dir ./gdm-output

# With custom degradation schema
python scripts/grassland_degradation_monitor.py \
  --years 10 \
  --degradation-schema references/degradation_schema.json \
  --output-dir ./gdm-output
```

## License

MIT
