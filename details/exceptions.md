# Retours d'erreur

## Format

```ts
{
    code: ErrorCode,
    description: string
}
```

**Exemple**

```json
{
    "code": "MISSING_PARAM",
    "description" : "Missing parameter 'birthDate'."
}
```

## Types

| `ErrorCode`            | statut HTTP | description                                                                          |
| ---------------------- | ----------- | ------------------------------------------------------------------------------------ |
| `MISSING_PARAMETER`    | 400         | un paramètre (URL, header, JSON, etc.) est manquant                                  |
| `INVALID_PARAMETER`    | 400         | un paramètre (URL, header, JSON, etc.) est invalide (vide, négatif, trop long. etc.) |
| `NOT_PERMITTED`        | 400         | une action n'est pas permise à l'instant présent                                     |
| `ITEM_NOT_FOUND`       | 404         | un élément est introuvable (id invalide ou inexistant)                               |

> L'exception pour le statut 500 n'est pas inscrite ici car elle devrait en principe ne jamais être retournée par le serveur.

## Détails additionnels

- Un paramètre "*manquant*" correspond à une valeur inexistante (champs non présent) ou nulle (`Null` en Java ou `null` en JSON).
- Un paramètre "*vide*" correspond à une valeur dont le contenu est "vide" (ex: string vide `""` ou contenant seulement des caractères "vide" (`'\t'`, `'\n'`, `' '`, etc.)).
- Lorsqu'un paramètre est nullable (avec `| null` après sont type), alors ce dernier peut être manquant sans générer d'erreur.
- Un champ non nullable doit retourner une erreur de type `MISSING_PARAMETER` si la valeur reçue est manquante.
- Par défaut, une valeur vide ne doit pas retourner d'exception (sauf si explicitement décrit dans les énoncés de features).
- Tous les paramètres d'URL (query params) sont optionels et peuvent donc être manquants sans retourner d'erreur.
- Les valeurs "vides" des paramètres d'URL (ex: "") doivent être considérées comme étant des vraies valeurs (ex: filtrer par `title = ""` doit retourner les titres égals à `""`).
