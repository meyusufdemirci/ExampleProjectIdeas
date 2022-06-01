Are you struggling to find a project to make progress in your iOS career? Here is the document that tells you project ideas from the beginning to the advanced tier.  

Please focus on and learn the keywords deeply in the project descriptions!

If you indent to get the best result, follow the projects by order. Do not jump from the first project to the fifth one.

# Projects
- [Calculator](#calculator)
- [To-Do List](#to-do-list)

## Calculator
Build a simple single-page calculator.  
It should have numbers from 0 to 9, plus, minus, divide, and multiply buttons with their actions.  
Also, a label to show the result of the process.
  
#### Goals
- Get familiar with communication between the controller and its view
- Alig UI components regularly
- Understand the logic mechanism in the controller
- Make a meaningful, tidy folder structure
  
#### Architecture
Use the pure MVC which is the simplest architecture in iOS development. No need for a view model.
  
#### Language / Framework
Swift with UIKit. No need to use SwiftUI for now.
  
#### Responsive Design
Use only one storyboard. Make all design processes in a single storyboard. No need to create separated storyboards or xib files.  
Fill the buttons on the screen by using horizontal and vertical stack views.  
Use constraints to make a dynamic sized stack view.
You are free to align the buttons as you wish.
  
#### Keywords
- MVC
- Storyboard
- Auto Layout
- StackView

## To-Do List
Build a three-page to-do list app that is similar to Apple's native Reminder app.  
It will have two screens. The first one is the list screen includes to-dos with their description, date, and time. Each to-do has a check button to make it completed.  
By tapping the plus(create) button, the create to-do screen opens. Users can define a description, date, and time on the to-do. A create button provides saving the to-do and it will be seen in the list on the list screen.  
In case the user taps on one of the to-dos, the detail page shows, and the user can edit the to-do.

#### Goals
- Understand MVVM
- Use table view
- Integrate third-party library
- Build UI programmatically
- Use model(such as ToDo)

#### Architecture
Use simple MVVM. No need to use protocols for now. Do not forget that **you must not import UIKit in the view model**.

#### Language / Framework
Swift with UIKit

#### Responsive Design
Integrate [SnapKit](https://github.com/SnapKit/SnapKit) via **SPM** and build UI programmatically. No need to use any Storyboard od xib files.  
Use table view in the list screen.  
You are free to build UI as you wish.

#### Keywords
- MVVM
- Table view
- SPM
- SnapKit
