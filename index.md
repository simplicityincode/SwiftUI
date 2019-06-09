## Learning Swift UI

This page was created to explore Apple's (WWDC 2019) newly introduced SwiftUI Framework.

### Basic View

This is how a basic view looks like:

```swift
struct ContentView: View {
  var body: some View {
    
  }
}

```

Here are some common modifiers for Text views:
```swift
struct ContentView: View {
  var body: some View {
    Text("Hello World")
      .font(.title)
      .font(.subheadline)
      .color(.green)
  }
}

```

Complex interfaces are created using Horizontal and Vertical Stacks:
```swift
struct ContentView: View {
    var body: some View {
        VStack(alignment: .leading) {
            ...
            HStack {
                ...
            }
        }
    }
}
```

Padding and Spaces:
```swift
  ..
  VStack {
  }.padding()
  Spacer()
```
