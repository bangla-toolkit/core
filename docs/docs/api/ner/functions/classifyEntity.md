# classifyEntity()

```ts
function classifyEntity(text): EntityType;
```

Defined in: [index.ts:68](https://github.com/nurulhudaapon/bntk/blob/4d05cddf73d9545c9d0917a84ef6563b6f925673/packages/core/ner/src/index.ts#L68)

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
