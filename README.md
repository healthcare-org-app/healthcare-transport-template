# healthcare-transport-template

Template repo for the Postman-in-the-terminal live demo ("from spec to a green PR in CI").
It holds only `openapi.yaml`: the spec of `transport-service` (non-emergency patient rides, 4 endpoints).
Do not modify it: the demo setup clones a disposable repo from this template for each run.
Never push demo work here; work in the throwaway clone.

## Lancer la démo en local

Les commandes `postman` de la démo restent locales : rien n'est écrit dans le cloud Postman.

1. Avant de commencer, exécuter `unset POSTMAN_API_KEY`, pour qu'aucune commande ne puisse atteindre le cloud par accident.
2. Initialiser avec `env -u POSTMAN_API_KEY postman init --json < /dev/null`, sans `--yes` ni `--visibility`.
3. Enchaîner dans cet ordre : init, génération de la collection, génération du mock, puis exécution de la collection sur le mock.
