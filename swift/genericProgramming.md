# [WIP] Generic Programming

###### Place holder:

`T` is the place holder. It will be contained in `<>`.

```swift
func p<T>(value: T) {
    // ...
}
```

We can even add constraint after the place holder.

```swift
func basicGeneric<T: CustomStringConvertible>(_ value: T) {
    print("Value: \(value)")
}
```

Or add constraint at the end:

```swift
func basicGeneric<T: CustomStringConvertible>(_ value: T) {
    print("Value: \(value)")
}
```
