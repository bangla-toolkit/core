# getEntityConfidence()

```ts
function getEntityConfidence(text, entityType): number;
```

Defined in: [index.ts:81](https://github.com/nurulhudaapon/bntk/blob/ee2db1ae9750affdceaef42403c2c985a2aa2e6d/packages/core/ner/src/index.ts#L81)

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
