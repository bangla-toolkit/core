# batchExtractEntities()

```ts
function batchExtractEntities(texts): Entity[][];
```

Defined in: [index.ts:96](https://github.com/nurulhudaapon/bntk/blob/25c5fe4c3c5aa822d37005be7e1fb5bdb0e245fe/packages/core/ner/src/index.ts#L96)

Processes multiple texts for entity extraction in batch.

## Parameters

| Parameter | Type       | Description               |
| --------- | ---------- | ------------------------- |
| `texts`   | `string`[] | Array of texts to process |

## Returns

[`Entity`](../interfaces/Entity.md)[][]

Array of entity arrays for each input text

## Example

```ts
const results = batchExtractEntities(["John Doe", "New York"]);
// Returns: [[{text: "John Doe", ...}], [{text: "New York", ...}]]
```
