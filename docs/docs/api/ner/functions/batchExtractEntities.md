# batchExtractEntities()

```ts
function batchExtractEntities(texts): Entity[][];
```

Defined in: [index.ts:96](https://github.com/nurulhudaapon/bntk/blob/ee2db1ae9750affdceaef42403c2c985a2aa2e6d/packages/core/ner/src/index.ts#L96)

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
