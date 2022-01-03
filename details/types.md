# Types généraux

### `Date`

Représente une date, en `string`, dans le format ISO-8601.

**Examples**

- `"2020-05-01"`

### `DateTime`

Représente une date ET une heure, au timezone explicite UTC, en `string`, dans le format ISO-8601.

**Examples**

- `"2020-05-01T22:49:56.917Z"`

### `Amount`

Représente un montant d'argent, avec arrondi standard à 2 décimales. Les décimales sont facultatives lorsque le nombre est entier. Le montant est représenté en `double` lorsque formatté.

**Exemples**

- `36.92`
- `52.00` ou `52.0` ou `52`

### `Email`

Représente une adresse e-mail, sous le format `<identifiant>@<service>.<extension>`, en `string`. `<identifiant>`, `<service>` et `<extension>` doivent être d'au moins 1 caractère.

**Examples**

- `"john.doe@gmail.com"`
- `"a@g.c"`

### `PhoneNumber`

Représente un numéro de téléphone, en `string`, sous le format international (11 chiffres), sans caractères spéciaux.

**Exemples**

- ~~+1 819 123 4567~~ => `"18191234556"`

### `ProductCategory`

Représente la catégorie d'appartenance à un produit, en `string`. Les valeurs permises sont :

- `"sports"`
- `"electronics"`
- `"apparel"`
- `"beauty"`
- `"housing"`
- `"other"`

### `SaleStatus`

Représente le statut d'une vente de produit, en `string`. Les valeurs permises sont :

- `"ongoing"`
- `"sold"`

## Références

- RFC-3339 \[[1](https://datatracker.ietf.org/doc/html/rfc3339)\] et ISO-8601 \[[1](https://www.w3.org/TR/NOTE-datetime)\] \[[2](https://www.loc.gov/standards/datetime/iso-tc154-wg5_n0038_iso_wd_8601-1_2016-02-16.pdf)\]: Références pour les format *date* et *datetime* standards
