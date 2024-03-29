# Identifiers

```ts
const is_a_value = 4;

// typealias
type is_a_type = {};

// namespace
namespace is_a_namespace {
  const foo = 17;
}
```

- `is_a_value` is an identifier for a constant value set to `4`.

- `is_a_type` is an identifier for a `type alias` representing an `empty object`.

- `is_a_namespace` is an identifier for a namespace containing a constant `foo`.

---

```ts
const x_2 = is_a_type; //! Wrong position for type
const x_3 = is_a_namespace; //✔️ Namespace can be used as a value

// how to test for a type
const y: is_a_value = {}; //! Wrong position for value
const yy: is_a_namespace = {}; // ✔️ Namespace can't be used as a type
```
