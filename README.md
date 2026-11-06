# healthcare-transport-template

Template repo for the Postman-in-the-terminal live demo ("from spec to a green PR in CI").
It holds only `openapi.yaml`: the spec of `transport-service` (non-emergency patient rides, 4 endpoints).
Do not modify it: the demo setup clones a disposable repo from this template for each run.
Never push demo work here; work in the throwaway clone.

## Run the demo locally

The demo's `postman` commands stay local: nothing is written to the Postman cloud.

1. Before starting, run `unset POSTMAN_API_KEY` so no command can reach the cloud by accident.
2. Initialize with `env -u POSTMAN_API_KEY postman init --json < /dev/null`, without `--yes` or `--visibility`.
3. Follow this sequence: init, generate the collection, generate the mock, then run the collection against the mock.
