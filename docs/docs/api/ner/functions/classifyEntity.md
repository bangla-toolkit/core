# classifyEntity()

```ts
function classifyEntity(text): EntityType;
```

Defined in: [index.ts:68](https://github.com/nurulhudaapon/bntk/blob/bd66ef90e0013a2d48aa5c6a9076fca8f447b329/packages/core/ner/src/index.ts#L68)

Classifies a single text segment into an entity type.

## Parameters

| Parameter | Type     | Description          |
| --------- | -------- | -------------------- |
| `text`    | `string` | The text to classify |

## Returns

[`EntityType`](../enumerations/EntityType.md)

The predicted entity type

## Example

```ts
const type = classifyEntity("John Doe");
// Returns: EntityType.PERSON
```
