### Event Sourcing

 - Source de données immutable
 - Stockage de l'historique des événements du domaine


### Event Sourcing

 - Protection

```
f(history) => state
f(state, command) => events
```

 - Interprétation

```
f(events) => state
```
Ou pour traiter chaque événement
```
f(state, event) => state
```
