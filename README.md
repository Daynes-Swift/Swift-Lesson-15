# Lesson 15 - Defining Structures

# Exercise: Your Own Structure
When you worked through the Types playground, you had a chance to think about some real-world examples of types and the associated types they might depend on. A TrainingShoe type, for example, might have a size property that's an Int, a brandName that's a String, and a releaseDate that's a Date.

## Exercise
Think of another real-world object and its properties. Make up some actions or behaviors that the object might be able to perform. Write them all in plain English first in a comment:

```swift
// Computer struct
// screenSize property: Double
// totalRamInMB: Int
// isOn: Bool
// manufacturer: String
// manufactureDate: Date
// turnOn function
// open(program: String) function
```

## Exercise

Using the struct syntax from this lesson, create a type for your real-world object with the properties and methods you thought of. Remembering to mark each property with let or var depending on whether or not it will be allowed to change. If you're not sure how to implement the body of one of the methods, describe what the method should do in a comment.
Hint: If you made any properties with custom types, you can create placeholder types that have empty implementations. (See the TrainingShoe code at the bottom of this page for an example.) The placeholder type below will make sure your playground can run without errors.

```swift
import Foundation

struct Computer {
    let screenSize: Double
    var totalRamInMB: Int
    var isOn: Bool
    let manufacturer: String
    let manufactureDate: Date
    
    mutating func turnOn() {
        print("Powering On!")
        isOn = true
    }
    
    func open(program: String) {
        if isOn {
            print("Opening the \(program) program")
        } else {
            print("The computer needs to be turned on before you can open \(program).")
        }
    }
}
```

## Exercise

Use the struct you created to make a new instance of your type.

```swift
var macbook = Computer(screenSize: 13.6, totalRamInMB: 8192, isOn: false, manufacturer: "Apple", manufactureDate: Date(timeIntervalSince1970: 1_387_584_000))
macbook.turnOn()
macbook.open(program: "VSCode")

// Output: 
// Powering On!
// Opening the VSCode program
```
