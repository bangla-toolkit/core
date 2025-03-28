# extractEntities()

```ts
function extractEntities(text): Entity[];
```

Defined in: [index.ts:41](https://github.com/nurulhudaapon/bntk/blob/25c5fe4c3c5aa822d37005be7e1fb5bdb0e245fe/packages/core/ner/src/index.ts#L41)

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
