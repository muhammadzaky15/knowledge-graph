# Knowledge Graph Visualization POC

Simple D3.js proof-of-concept for visualizing Indonesia regulation data in three layouts:

- Force-directed graph
- Timeline constrained to regulation `year`
- Columns grouped by `hierarchy_name`

Nodes show regulation titles, hierarchy-based fills, and status-colored borders. Directed edges display relationship `type` labels and inherit colors from the target node's status.

## Prerequisites

- Node.js 16+ (only for running a static server; no build tools required)

## Running locally

```bash
cd /Users/arkka/Workspaces/hukumonline/poc-kg-visualization
npx serve .
```

Then open the URL printed in the terminal (for example, `http://localhost:3000/index.html`). Loading via `file://` will fail because browsers block `fetch` requests to local JSON files.

## Files

- `sample-data-500.json` – graph dataset exported from the regulation knowledge graph.
- `index.html` – self-contained D3 visualization that reads the JSON directly and exposes layout toggle buttons plus legend/tooltip.

