---
title: Set.ts
nav_order: 80
parent: Modules
---

# Set overview

Added in v2.0.0

---

<h2 class="text-delta">Table of contents</h2>

- [chain (constant)](#chain-constant)
- [compact (constant)](#compact-constant)
- [difference (constant)](#difference-constant)
- [elem (constant)](#elem-constant)
- [empty (constant)](#empty-constant)
- [every (constant)](#every-constant)
- [filterMap (constant)](#filtermap-constant)
- [foldMap (constant)](#foldmap-constant)
- [fromArray (constant)](#fromarray-constant)
- [getEq (constant)](#geteq-constant)
- [getIntersectionSemigroup (constant)](#getintersectionsemigroup-constant)
- [getShow (constant)](#getshow-constant)
- [getUnionMonoid (constant)](#getunionmonoid-constant)
- [insert (constant)](#insert-constant)
- [intersection (constant)](#intersection-constant)
- [map (constant)](#map-constant)
- [partitionMap (constant)](#partitionmap-constant)
- [reduce (constant)](#reduce-constant)
- [remove (constant)](#remove-constant)
- [separate (constant)](#separate-constant)
- [singleton (constant)](#singleton-constant)
- [some (constant)](#some-constant)
- [subset (constant)](#subset-constant)
- [toArray (constant)](#toarray-constant)
- [union (constant)](#union-constant)
- [filter (function)](#filter-function)
- [partition (function)](#partition-function)

---

# chain (constant)

**Signature**

```ts
export const chain: <B>(E: Eq<B>) => <A>(f: (x: A) => Set<B>) => (set: Set<A>) => Set<B> = ...
```

Added in v2.0.0

# compact (constant)

**Signature**

```ts
export const compact: <A>(E: Eq<A>) => (fa: Set<Option<A>>) => Set<A> = ...
```

Added in v2.0.0

# difference (constant)

Form the set difference (`x` - `y`)

**Signature**

```ts
export const difference: <A>(E: Eq<A>) => (x: Set<A>, y: Set<A>) => Set<A> = ...
```

**Example**

```ts
import { difference } from 'fp-ts/lib/Set'
import { eqNumber } from 'fp-ts/lib/Eq'

assert.deepStrictEqual(difference(eqNumber)(new Set([1, 2]), new Set([1, 3])), new Set([2]))
```

Added in v2.0.0

# elem (constant)

Test if a value is a member of a set

**Signature**

```ts
export const elem: <A>(E: Eq<A>) => (a: A, set: Set<A>) => boolean = ...
```

Added in v2.0.0

# empty (constant)

**Signature**

```ts
export const empty: Set<never> = ...
```

Added in v2.0.0

# every (constant)

**Signature**

```ts
export const every: <A>(predicate: Predicate<A>) => (set: Set<A>) => boolean = ...
```

Added in v2.0.0

# filterMap (constant)

**Signature**

```ts
export const filterMap: <B>(E: Eq<B>) => <A>(f: (a: A) => Option<B>) => (fa: Set<A>) => Set<B> = ...
```

Added in v2.0.0

# foldMap (constant)

**Signature**

```ts
export const foldMap: <A, M>(O: Ord<A>, M: Monoid<M>) => (f: (a: A) => M) => (fa: Set<A>) => M = ...
```

Added in v2.0.0

# fromArray (constant)

Create a set from an array

**Signature**

```ts
export const fromArray: <A>(E: Eq<A>) => (as: Array<A>) => Set<A> = ...
```

Added in v2.0.0

# getEq (constant)

**Signature**

```ts
export const getEq: <A>(E: Eq<A>) => Eq<Set<A>> = ...
```

Added in v2.0.0

# getIntersectionSemigroup (constant)

**Signature**

```ts
export const getIntersectionSemigroup: <A>(E: Eq<A>) => Semigroup<Set<A>> = ...
```

Added in v2.0.0

# getShow (constant)

**Signature**

```ts
export const getShow: <A>(S: Show<A>) => Show<Set<A>> = ...
```

Added in v2.0.0

# getUnionMonoid (constant)

**Signature**

```ts
export const getUnionMonoid: <A>(E: Eq<A>) => Monoid<Set<A>> = ...
```

Added in v2.0.0

# insert (constant)

Insert a value into a set

**Signature**

```ts
export const insert: <A>(E: Eq<A>) => (a: A) => (set: Set<A>) => Set<A> = ...
```

Added in v2.0.0

# intersection (constant)

The set of elements which are in both the first and second set

**Signature**

```ts
export const intersection: <A>(E: Eq<A>) => (set: Set<A>, y: Set<A>) => Set<A> = ...
```

Added in v2.0.0

# map (constant)

Projects a Set through a function

**Signature**

```ts
export const map: <B>(E: Eq<B>) => <A>(f: (x: A) => B) => (set: Set<A>) => Set<B> = ...
```

Added in v2.0.0

# partitionMap (constant)

**Signature**

```ts
export const partitionMap: <B, C>(
  EB: Eq<B>,
  EC: Eq<C>
) => <A>(f: (a: A) => Either<B, C>) => (set: Set<A>) => Separated<Set<B>, Set<C>> = ...
```

Added in v2.0.0

# reduce (constant)

**Signature**

```ts
export const reduce: <A>(O: Ord<A>) => <B>(b: B, f: (b: B, a: A) => B) => (fa: Set<A>) => B = ...
```

Added in v2.0.0

# remove (constant)

Delete a value from a set

**Signature**

```ts
export const remove: <A>(E: Eq<A>) => (a: A) => (set: Set<A>) => Set<A> = ...
```

Added in v2.0.0

# separate (constant)

**Signature**

```ts
export const separate: <E, A>(
  EE: Eq<E>,
  EA: Eq<A>
) => (fa: Set<Either<E, A>>) => Separated<Set<E>, Set<A>> = ...
```

Added in v2.0.0

# singleton (constant)

Create a set with one element

**Signature**

```ts
export const singleton: <A>(a: A) => Set<A> = ...
```

Added in v2.0.0

# some (constant)

**Signature**

```ts
export const some: <A>(predicate: Predicate<A>) => (set: Set<A>) => boolean = ...
```

Added in v2.0.0

# subset (constant)

`true` if and only if every element in the first set is an element of the second set

**Signature**

```ts
export const subset: <A>(E: Eq<A>) => (x: Set<A>, y: Set<A>) => boolean = ...
```

Added in v2.0.0

# toArray (constant)

**Signature**

```ts
export const toArray: <A>(O: Ord<A>) => (set: Set<A>) => Array<A> = ...
```

Added in v2.0.0

# union (constant)

Form the union of two sets

**Signature**

```ts
export const union: <A>(E: Eq<A>) => (set: Set<A>, y: Set<A>) => Set<A> = ...
```

Added in v2.0.0

# filter (function)

**Signature**

```ts
export function filter<A, B extends A>(refinement: Refinement<A, B>): (set: Set<A>) => Set<B>
export function filter<A>(predicate: Predicate<A>): (set: Set<A>) => Set<A> { ... }
```

Added in v2.0.0

# partition (function)

**Signature**

```ts
export function partition<A, B extends A>(refinement: Refinement<A, B>): (set: Set<A>) => Separated<Set<A>, Set<B>>
export function partition<A>(predicate: Predicate<A>): (set: Set<A>) => Separated<Set<A>, Set<A>> { ... }
```

Added in v2.0.0
