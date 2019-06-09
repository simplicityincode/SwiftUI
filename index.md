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
  VStack {
    ...
  }.padding()
  Spacer()
```

Images:
```swift
        ...
        Image("turtlerock")
            .clipShape(Circle())
            .overlay(
                Circle().stroke(Color.gray, lineWidth: 4))
            .shadow(radius: 10)
            .offset(y: -130)
            .padding(.bottom, -130)
        ...
    
```

Use UIKit and SwiftUI Views Together:
```swift
import SwiftUI
import MapKit

struct MapView: UIViewRepresentable {
    func makeUIView(context: Context) -> MKMapView {
        MKMapView(frame: .zero)
    }

    func updateUIView(_ view: MKMapView, context: Context) {
        let coordinate = CLLocationCoordinate2D(
            latitude: 34.011286, longitude: -116.166868)
        let span = MKCoordinateSpan(latitudeDelta: 2.0, longitudeDelta: 2.0)
        let region = MKCoordinateRegion(center: coordinate, span: span)
        view.setRegion(region, animated: true)
    }
}
```
