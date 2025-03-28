# getEntityConfidence()

```ts
function getEntityConfidence(text, entityType): number;
```

Defined in: [index.ts:81](https://github.com/nurulhudaapon/bntk/blob/25c5fe4c3c5aa822d37005be7e1fb5bdb0e245fe/packages/core/ner/src/index.ts#L81)

Calculates confidence score for entity classification.

## Parameters

| Parameter    | Type                                          | Description              |
| ------------ | --------------------------------------------- | ------------------------ |
| `text`       | `string`                                      | The text to analyze      |
| `entityType` | [`EntityType`](../enumerations/EntityType.md) | The entity type to check |

## Returns

`number`

Confidence score between 0 and 1

## Example

```ts
const confidence = getEntityConfidence("John Doe", EntityType.PERSON);
// Returns: 0.85
```
