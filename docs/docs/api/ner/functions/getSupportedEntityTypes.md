# getSupportedEntityTypes()

```ts
function getSupportedEntityTypes(): EntityType[];
```

Defined in: [index.ts:107](https://github.com/nurulhudaapon/bntk/blob/ee2db1ae9750affdceaef42403c2c985a2aa2e6d/packages/core/ner/src/index.ts#L107)

Retrieves all supported entity types.

## Returns

[`EntityType`](../enumerations/EntityType.md)[]

Array of all supported entity types

## Example

```ts
const types = getSupportedEntityTypes();
// Returns: [EntityType.PERSON, EntityType.ORGANIZATION, ...]
```
