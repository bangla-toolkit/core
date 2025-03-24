# getEntityConfidence()

```ts
function getEntityConfidence(text, entityType): number;
```

Defined in: [index.ts:81](https://github.com/nurulhudaapon/bntk/blob/bd66ef90e0013a2d48aa5c6a9076fca8f447b329/packages/core/ner/src/index.ts#L81)

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
