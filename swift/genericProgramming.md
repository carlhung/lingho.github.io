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
you can also constraint to multiple protocols or a class:
```swift
func basicGeneric<T: CustomStringConvertible & Hashable>(_ value: T) {
    print("Value: \(value)")
}

func basicGeneric1<T>(_ value: T) where T: CustomStringConvertible & Hashable {
    print("Value: \(value)")
}

func basicGeneric2<T>(_ value: T) where T: CustomStringConvertible, T: Hashable {
    print("Value: \(value)")
}

func basicGeneric3<C, D>(_ value1: C, _ value2: D) where C: Collection, C.Element: CustomStringConvertible, D: Collection, D.Element == C.Element {
    print("Value1: \(value1), value2: \(value2)")
}

func basicGeneric4<C: Collection, D: Collection>(_ value1: C, _ value2: D) where C.Element: CustomStringConvertible, D.Element == C.Element {
    print("Value1: \(value1), value2: \(value2)")
}
```