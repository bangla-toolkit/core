# tagWord()

```ts
function tagWord(word): TaggedWord;
```

Defined in: [index.ts:102](https://github.com/nurulhudaapon/bntk/blob/25c5fe4c3c5aa822d37005be7e1fb5bdb0e245fe/packages/core/pos/src/index.ts#L102)

Tags a single Bangla word with its part of speech

## Parameters

| Parameter | Type     | Description            |
| --------- | -------- | ---------------------- |
| `word`    | `string` | The Bangla word to tag |

## Returns

[`TaggedWord`](../interfaces/TaggedWord.md)

The word with its POS tag and features

## Description

This function performs POS tagging for a single Bangla word.
It uses a combination of rules and dictionary lookup to determine
the most likely POS tag for the given word.

## Examples

```typescript
const result = tagWord("বাংলা");
console.log(result);
// Output: { word: "বাংলা", tag: UniversalPOSTag.NOUN }
```

```typescript
const result = tagWord("সুন্দর");
console.log(result);
// Output: { word: "সুন্দর", tag: UniversalPOSTag.ADJ }
```
