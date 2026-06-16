# resource-agent-factory

TellMesh agent generation core — NL → contract → generated agent packages under `agents/generated/`.

Extracted from [tellmesh/tellmesh](https://github.com/tellmesh/tellmesh).

```text
nl2uri / nl2a / uri ecosystem -> proposal -> agents/generated/* + deployments
hypervisor -> run-agent, health, describe-agent
```

## Install

```bash
uv sync
pytest tests/ -q
```

## CLI quickstart

```bash
nl2a generate -p "weather map agent with health endpoint" --out output/agents/weather
hypervisor deployments   # after registering in agent_deployments.yaml
hypervisor run-agent weather-map-agent.local --detach --wait-healthy
```

## Examples

| Example | Path |
|---------|------|
| NL → weather agent | [`tellmesh/examples/04_nl2a_weather_map`](../tellmesh/examples/04_nl2a_weather_map) |
| Invoices agent | [`tellmesh/examples/07_invoices_agent`](../tellmesh/examples/07_invoices_agent) |
| NL tutorial | [`tellmesh/examples/23_nl_to_agent_tutorial`](../tellmesh/examples/23_nl_to_agent_tutorial) |

## Links

- [TODO](TODO.md)
- [resource-agent-hypervisor](../resource-agent-hypervisor)
- [urigen](../urigen) (ecosystem generator)
- Org status: [`../TODO_STATUS.md`](../TODO_STATUS.md)

## License

Licensed under Apache-2.0.
