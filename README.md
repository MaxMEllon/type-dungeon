<!-- This is a generated file. Don't touch directly! -->

# Type Dungeon

### to-strict

Play this with <a href="https://www.typescriptlang.org/v2/play?#code/PTAEFEBMEsBdVgCwKagE7QOaPoghgHaSgDO0kqsA9qALZ6wDGiCKoAZlQDZdUDu0AplDIAHgAdkjWMmKwAnpNCMqRONFUkAdACgFSgMqwM0gDwAVAHygAvKACuBANYF+BANw6dICBKkzIL31UAypaZAB5ACMAK39zRVQ7AG8dUFACPHCAfgAuUmNBTE90vExkPIz7WijkNE8AX08dCkYuPDRUFQISeF6TWGiY-KMB01DwofjEy2bu3oys5Hz+otsCgaGtTPD3UB9gqnZF8NJEKnsuYld4WociZHZBWX2qnh15+DLlqpq69dW0i23z2B0SR1A3zOFyuGSot1QjgoTwILzABEuXB0QA" target="_blank">TypeScript playground</a> !

```typescript
// Edit the right hand side to match the following expected type conditions.
type Strict<T> = unknown;

// Expected

type SomeObjectType = {
  name?: string;
  age?: number;
};

declare const strictObj: Strict<SomeObjectType>;

const name: string = strictObj.name; // typeof name should not be undefined / null
const age: number = strictObj.age; // typeof age should not be undefined / null
```

<a href="https://www.typescriptlang.org/v2/play?#code/C4TwDgpgBAysBOBLAxsAPAFQHxQLxQG8oBtABSkQDsoBrCEAewDMoMBdAWgH4AuVstlAC+AbgBQYgPSSoAUQAekVBAAmE0JFgMAthADyAIwBWEVBnDR8BMVCiUAhrt5QAzgioBzcbfseIzygBXbQMIeHFRCRVTABt7eGhkBko3V3dUQyM+OCRUNBgdfWNTYHNILHExJJTgO0cIPjckSg88NNzgTIA6B10RKGkoDQhmOt1XAAsGQJiVOwZa0KhAymimKlUBuxmYquTU3wbtkLC2ppRO4y7D-sHh0cPJ6dn5xegVtY25mSCY3aA" target="_blank">
  Check out the answer.
</a>
  
### awaited

Play this with <a href="https://www.typescriptlang.org/v2/play?#code/PTAEFEBMEsBdVgCwKagE7QOaPoghgHaSgDO0kqsA9qALZ6wDGiCKoAZlQDZdUDu0AplDIAHgAdkjWMmKwAnpNCMqRONFUkAdACgFSgIJ88cWQB4AKgD5QAXlCF5Abh17FqAAoBGO6A9oqWmgSZDMSWAwhKxd9TwAmX39A4NCkoJCwiMFMK2jXEBEJKRlINyUAZR97IxMSs29o0AKSRCoAVy5iACNUcMjMGPdQcoTq41NIerjG5sQ2ju7erKEEKioXIA" target="_blank">TypeScript playground</a> !

```typescript
// Edit the right hand side to match the following expected type conditions.
type Awaited<T> = any;

type P1 = Promise<string>;
type P2 = Promise<Promise<string>>;

// expected
type S1 = Awaited<P1>; // should be string;
type S2 = Awaited<P2>; // shuuld be string too;
```

<a href="https://www.typescriptlang.org/v2/play?#code/C4TwDgpgBAgg7gQwJbAgEwDwBUB8UC8UAFFlBAB6oB2aAzlAAoBOA9gLZK0QAySA1hAxIqAMwhMoADTwB+KAG8oABgBcsRCnQZpUAL5Q1i1VFK6AlAG0lAXQDcAKHuhIjAIwFGrDlwy1gTYQBzHAdnaAYAJg9mdk5BGO9BPwCqYJDHAHoMsnJIAGNUNCdwaABld0J4ZEKMBlcQqCyoWgALFgBXABs0KAAjaGSg0JKoUqjKjRrIhqbW9q6e-ub-IKhgFhYHIA" target="_blank">
  Check out the answer.
</a>
  
### curry

Play this with <a href="https://www.typescriptlang.org/v2/play?#code/PTAEGEHsFsAcBsCmAXRpkAs0DMCuA7AY2QEtJ90BPWNZSUaAQ2UI3S1G0nnkgHcS+AOahEADxrFEAEyo1QhctJKlyAOgBQ0xIXiMATjgLEyFQrn37KACmz4AXKABix1fgCUjxvkoBuDRogoACiEjqo0gGK+ADOyKCM0rIAvKDWjI74uNAARoj6ADSgOZnZefruoMkAfAmgANTF-tFxxZAEKQoWVulJ7tYAjO7+Oe340tbDoEExGO3wspj6-KKWkPoaox2DAAw7RQN7UzNzuAvsy3yryxsaLfEAbozwuIiluflVbduHO8dgs3msgAcgB5AAqFxW+RuGiAA" target="_blank">TypeScript playground</a> !

```typescript
// Complete the function type to match the following expected type condition.
declare function curry(fn: Function): any;

// Expected

const add = (a: number, b: number) => a + b;
const bound = curry(add)(1);
bound(); // should throw error
bound(100, 100); // should throw error

const value: number = bound(100); // should NOT throw error
```

<a href="https://www.typescriptlang.org/v2/play?#code/CYUwxgNghgTiAEAzArgOzAFwJYHtXzGRhgE8AeAFXhAA8MRVgBneAMTU11QD4AKAKHhJUALngUANPwCUYqrXqMWvKGKypEIGPACCE+ADojcJhjUat8AELT4AXm7x1m7QCV4AfngqxO2w+8jA1gAcyYxG3tHdzFUEAA3LQBufn4AejT4AFEaAAdwemBUsDxTeChgYHtvVXhUZABbACMtfSbYxpaYf0coeABqeCaUktQyppw0KrsCIlIVSuleAEZpFImp3jX4DPgmAAtJiCqMfZgcAHdqYhwYfg3GFYAGJ-1ll+3dg6OTs8vr853fijMrxKAQZAgDrNSwzB7AZ5PT6Zb7IY7wAByAHkqKdzlctID+EA" target="_blank">
  Check out the answer.
</a>
  
### randomize

Play this with <a href="https://www.typescriptlang.org/v2/play?#code/PTAEGEHsFsAcBsCmAXRpkAs0AMBKBDAOwBMZt0BPWRAOgChkq0CSZQBeUAV0IGtDIAd0IBuOnWKIAxvHwAnNFMiEAzslByipaAC5QLbWLpLV6-B1ABvUADd88Loj0BGUAF9Q+FaBNqxv9QAjC2s7BydQACZ3T28A-2U1HxDbe0c9AGYYrx9E5CMQUABRAA9qKVRiHTpCgBUsUGxNVmhyBWQuOUJKalAVDEgueGJQQLQvFQBLAHNCfECkdAxJ70ZeogFkfGRJ5XoA1PC9ULSI1w8AHytD9KiYq5Oj0CyPTmbtAAp8ABpR36kAJRiIA" target="_blank">TypeScript playground</a> !

```typescript
// Complete the `Random` type.
type Random = unknown;

declare const random: Random;

const a = { value: 1 } as const;
const b = { value: 2 } as const;
const c = { value: 3 } as const;

// Expected:
// The `random` return type should be assignable this type annotation.
const value: { value: 1 } | { value: 2 } | { value: 3 } = random(a, b, c);
```

<a href="https://www.typescriptlang.org/v2/play?#code/C4TwDgpgBAYgrgOwMYB4CCUC8UCGCQA0UASlrvgHxkAUOATgOYDOAXFGgJRZXEDcAUP1CQoAVQQBLAPYIUANSKioEAB7AICACZNyIANoBdKtgDe-KFAAMbOQIsBGNtWoA6NwDc2orpip4QXKrqWjrUABYQOJpsEggAZhB0UAASkZpEbi7AOBIANjHxiVAAKjm5Pn74UAD8YpIy8lAAPilpRKV5VGwIEO6JAgC+eqJ6AOS5GgzAYaMGymoa2lY1y2z2BgJC4NDEeJpSALZkKMWK88FL-oYU1HESdEzAbKdQmXQQBwh4T2IVddKyF6iCibTQQJC5ejQJAyR5QOh7Q5sXZaQ6bGEIOE4MgmKDuHC5OAQNZQAa4HQYx4CSnAKAAIxxeIJRLYACZSeSoDTqbDaUhGfjCcSoABmDk4Cm8zYAemlUAAoipIEh1NF+LKShEoAADBGog7a+EQYBwOgIKDCaBMMJSOC5TT06ASpgSBhfOkTC1hCQ6S3kBBSbLAAEufg0plCti4wUsqD2DktaPM4XssmJiOxsVk7B6-YHWhEOlEJAcARAA" target="_blank">
  Check out the answer.
</a>
  
## LICENSE
MIT
