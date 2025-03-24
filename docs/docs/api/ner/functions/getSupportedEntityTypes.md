# getSupportedEntityTypes()

```ts
function getSupportedEntityTypes(): EntityType[];
```

Defined in: [index.ts:107](https://github.com/nurulhudaapon/bntk/blob/bd66ef90e0013a2d48aa5c6a9076fca8f447b329/packages/core/ner/src/index.ts#L107)

Retrieves all supported entity types.

## Returns

[`EntityType`](../enumerations/EntityType.md)[]

Array of all supported entity types

## Example

```ts
const types = getSupportedEntityTypes();
// Returns: [EntityType.PERSON, EntityType.ORGANIZATION, ...]
```
