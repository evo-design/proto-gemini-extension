# Proto

Proto gives you access to a catalog of bioinformatics tools for generative biology. These
include protein language models, structure predictors, inverse folding, docking, and genomic
scorers. Tools run through the user's Proto account on their own Modal workspace.

## Workflow

1. Call `workspace_info` first. It shows the signed-in account and whether Modal is connected.
2. Find a tool with `search_tools` or `list_tools`. Pass `deployed_only=false` to see the full
   catalog, including tools that are not yet deployed.
3. Call `get_tool_schema`, then `get_tool_example`. Build inputs from the schema and example.
   Do not guess field names. Unknown fields are rejected.
4. Run the tool with `run_tool`. If it returns `pending`, collect the result with
   `get_run_status`. If a response never arrives, find the `job_id` with `list_runs` instead
   of running the tool again.
5. Cite the method with `get_tool_info` when you report a result.

## Cost and compute

Runs and deployments are billed to the user's Modal account. Ask the user before calling
`deploy_tool`. GPU tools need Modal connected at
https://proto.evodesign.org/settings/account/modal.

## Docs

https://proto.evodesign.org/docs/mcp/functions
