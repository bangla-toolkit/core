# extractEntities()

```ts
function extractEntities(text): Entity[];
```

Defined in: [index.ts:41](https://github.com/nurulhudaapon/bntk/blob/bd66ef90e0013a2d48aa5c6a9076fca8f447b329/packages/core/ner/src/index.ts#L41)

Extracts named entities from input text.

## Parameters

| Parameter | Type     | Description               |
| --------- | -------- | ------------------------- |
| `text`    | `string` | The input text to analyze |

## Returns

[`Entity`](../interfaces/Entity.md)[]

Array of detected entities with their positions and classifications

## Example

```ts
const entities = extractEntities("John Doe works at Apple Inc.");
// Returns: [{text: "John Doe", type: "PERSON", start: 0, end: 8, confidence: 0.95}]
```
