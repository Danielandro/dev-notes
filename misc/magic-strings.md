# Magic Strings

**Definition**

> Magic strings are string values that are specified directly within application code that have an impact on the application’s behavior.
> [DevIQ](https://deviq.com/magic-strings/)

Magic number are also a thing!

The solution is to refactor these values to use constants.

## Why?

- **Reusability** value can be used everywhere in app
- **Maintainability** easy to change - only one source of truth
- **Readability** easy for other devs to identify what value represents

## Example

**Bad**

```go
func sendSomethingToServer(data string) string {
  returnValue := sendToServer(data)
  switch returnValue {
    case 1: return "That's cool"
    case 3: return "That's bad"
    default: return "I have no idea"
  }
}

```

A dev reading this code may not know what 1 or means.

**Better**

```go
const responseOK = 1
const responseBad = 3

func sendSomethingToServer(data string) string {
  returnValue := sendToServer(data)
  switch returnValue {
    case responseOK: return "That's cool"
    case responseBad: return "That's bad"
    default: return "I have no idea"
  }
}
```

Definitely more readable, and easier to maintain

---

### Resources

- [Are magic strings/numbers always bad?](http://www.douevencode.com/articles/2017-11/magic-strings-not-always-bad/)

---

[Main Page](../README.md)
