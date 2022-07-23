Are you struggling to find a project to make progress in your iOS career? Here is the document that tells you project ideas from the beginning to the advanced tier.  

Please focus on and learn the keywords deeply in the project descriptions!

If you indent to get the best result, follow the projects by order. Do not jump from the first project to the fifth one.

# Projects
- [Calculator](#calculator)
- [To-Do List](#to-do-list)
- [Movies](#movies)
- [News](#news)

## Calculator
Build a simple single-page calculator.  
It should have numbers from 0 to 9, plus, minus, divide, and multiply buttons with their actions.  
Also, a label to show the result of the process.
  
#### Goals
- Get familiar with communication between the controller and its view
- Align UI components regularly
- Understand the logic mechanism in the controller
- Make a meaningful, tidy folder structure
  
#### Architecture
Use the pure MVC which is the simplest architecture in iOS development. No need for a view model.
  
#### Language / Framework
Swift with UIKit. No need to use SwiftUI for now.
  
#### Responsive Design
- Use only one storyboard. Make all design processes in a single storyboard. No need to create separated storyboards or xib files
- Fill the buttons on the screen by using horizontal and vertical stack views
- Use constraints to make a dynamic sized stack view
- You are free to align the buttons as you wish.

#### Logic
Insert outlets and actions of the buttons to the controller. Make the calculation by the operator. Use functions to make different calculations.
  
#### Keywords
- MVC
- Storyboard
- Auto Layout
- StackView

## To-Do List
Build a three-paged to-do list app that is similar to Apple's native Reminder app.  
It will have two screens. The first one is the list screen includes to-dos with their description, date, and time. Each to-do has a check button to make it completed.  
By tapping the plus(create) button, the create to-do screen opens. Users can define a description, date, and time on the to-do. A create button provides saving the to-do and it will be seen in the list on the list screen.  
In case the user taps on one of the to-dos, the detail page shows, and the user can edit the to-do.

#### Goals
- Understand MVVM by separating logic between controller and view model
- Learn to implement table view
- Integrate third-party library
- Build UI programmatically in controller
- Use model(such as ToDo) with Codable
- Use UserDefaults to fetch and save data locally

#### Architecture
Use simple MVVM. No need to use protocols for now. Do not forget that **you must not import UIKit in the view model**.

#### Language / Framework
Swift with UIKit

#### Responsive Design
- Integrate [SnapKit](https://github.com/SnapKit/SnapKit) via **SPM** and build UI programmatically. No need to use any Storyboard od xib files
- Use table view in the list screen
- You are free to build UI as you wish

#### Logic
Implement Codable to your To-Do model and store to-dos as an array in local by using UserDefaults.

#### Keywords
- MVVM
- Table view
- Codable
- SPM
- SnapKit
- UserDefaults

#### Tips
- Use **viewWillAppear** or **viewDidAppear** in the list screen to refresh the data

## Movies
Build a four-paged movie list app.  
It will have four screens. The first appearing screen is the splash screen. The data must be fetched from the [API](https://developers.themoviedb.org/3/getting-started/introduction) in here. As soon as the process is done, endirect the user to the app.
The first screen inside the app is the list screen that has list of movies with supporting search and filter. I can able to search by the name of the movie and filter by the category(the genres property in the movie object) of the movie. Each cell must at least have an image, title, and image of the movie.
By tapping one of the movies, the movie detail screen must appear. I can able to add the movie into the bookmarks via a button.
The last screen is the bookmarks which have the bookmarked movies. No need filter and search here, only a list.  
The list and bookmarks screens must be on a **TabBarController**. Tab bars' each first item must be **NavigationController**.  

#### Goals
- Understand Tab Bar and Navigation Controller
- Understand MVVM by separating logic between controller and view model
- Learn to implement table view
- Integrate third-party library
- Build UI programmatically in controller
- Use UserDefaults
- Integrate network layer by URLSession
- Use model(such as Movie) with Codable

#### Architecture
- Use simple MVVM. Do not forget that **you must not import UIKit in the view model**
- Use protocols to pass the data from the network layer to the screen

#### Language / Framework
Swift with UIKit

#### Responsive Design
- Integrate SnapKit to build UI programmatically. No need to use any Storyboard od xib files
- Use table view in the list screen
- Download movie images via [Kingfisher](https://github.com/onevcat/Kingfisher)

#### Logic
- The search and filter mechanism in the list screen must work without blocking UI
- Implement Codable to your Movie model and store movies as an array in a singleton object
- Store bookmarked movies in the UserDefaults as an array

#### Keywords
- MVVM
- Table view
- Codable
- SPM
- SnapKit
- Kingfisher
- Network layer
- URLSession
- Singleton
- UserDefaults

#### Note
This is one of the most essential projects since most of the companies ask this kind of case/challenge to understand your technical knowledge. Be more serious on this project than others!

## News
Build a four-paged news list app.  
It will have four screens. The first appearing screen is the splash screen. Ask push notification permission at splash.  
The second screen is the list that includes the news from now to the past. Fetch the data from [Google News API](https://newsapi.org/s/google-news-api). I can able to refresh the data by the pull to refresh.  
The list screen must have a search and filter which can work at the same time. I can able to search by text and filter by date range such as from 01/01/2022 to 30/01/2022. **The search must work with the API, not locale**.  
By tapping one of the news, the news detail screen must appear. I can able to add the news to the favorites via a button.  
The last screen is the favorites that have the favorite news. No need filter and search here, only a list. Store the favorites with their news title and source URL. Open Safari when a favorited news is tapped.  
Use TabBarController to store the list and favorites screens.

#### Goals
- Learn asking permission
- Learn how to use closures
- Understand MVVM by separating logic between controller and view model
- Integrate third-party library
- Build UI programmatically in controller
- Use UserDefaults
- Integrate generic network layer by Alamofire
- Use model(such as News) with Codable
- Understand localization
- Write unit test

#### Architecture
- Use simple MVVM. Do not forget that **you must not import UIKit in the view model**
- Use closures to communicate between controller and view model
- Build a generic network layer combined with Alamofire. Here is an [article](https://demirciy.medium.com/generic-network-layer-in-ios-development-2bffff780832) about it
- Use protocols to pass the data from the network layer to the screen

#### Language / Framework
Swift with UIKit

#### Responsive Design
- Integrate SnapKit to build UI programmatically. No need to use any Storyboard od xib files
- Use table view in the list screen
- Download news images via [Kingfisher](https://github.com/onevcat/Kingfisher)

#### Logic
- The push notification permission must be async in the splash screen. The screen waits for the user's response to show the next screen
- The search and filter mechanism in the list screen must work without blocking UI
- Store favorited news in the UserDefaults as an array
- Localize texts in at least two languages
- At least the view models and network layer must be covered by the unit test

#### Keywords
- MVVM
- Table view
- Codable
- SPM
- SnapKit
- Kingfisher
- Generic network layer
- Alamofire
- UserDefaults
- Localization
- Unit test
- Closure

#### Note
This is one of the most essential projects since most of the companies ask this kind of case/challenge to understand your technical knowledge. Be more serious on this project than others!
