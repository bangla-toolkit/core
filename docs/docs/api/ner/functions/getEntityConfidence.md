# getEntityConfidence()

```ts
function getEntityConfidence(text, entityType): number;
```

Defined in: [index.ts:81](https://github.com/nurulhudaapon/bntk/blob/3cb3d2a47ba842d629243298e3fd679945ac06fb/packages/core/ner/src/index.ts#L81)

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
