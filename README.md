# SwapiSdk
iOS SDK for Star Wars API https://swapi.dev/

## Demo
Clone the repo, open `SwapiSdk.xcworkspace` and run the Demo app to see the SDK in use

<img src=https://raw.githubusercontent.com/emmanuelkehinde/SwapiSdk/master/Docs/recording.gif width=300/>


## Requirements
- iOS 12.1 (SDK), iOS 14.1 (Demo)
- Xcode 10.1 (SDK), Xcode 12 (Demo)

## Installation

Here is how to integrate the library into your iOS project.

### Swift Package Manager

- File > Swift Packages > Add Package Dependency
- Add `https://github.com/emmanuelkehinde/SwapiSdk.git`
- Select "master" branch

### Cocoapods

- Pending release...

You can however build the sdk and integrate the `Swapi.framework` generated into your project.

## Basic Usage

The following functions are accessible through the `SwapiClient` class.

- `getFilms()`: To get all Starwars films, their title, opening crawl and the year they were released
- `getEyeColors()`: To get eye color of 5 different people from the Star Wars franchise
- `getPlanetsPopulation()`: To get the population of 5 different planets that list their population and climate

```swift
import Swapi

let swapiClient = SwapiClient()

// All Starwars films, their title, opening crawl and the year they were released
swapiClient.getFilms { films in
    print(films)
} onFailure: { error in
    print(error.localizedDescription)
}

// Eye color of 5 different people from the Star Wars franchise
swapiClient.getEyeColors { eyeColors in
    print(eyeColors)
} onFailure: { error in
    print(error.localizedDescription)
}

// Population of 5 different planets that list their population and climate
swapiClient.getPlanetsPopulation { planetsPopulation in
    print(planetsPopulation)
} onFailure: { error in
    print(error.localizedDescription)
}
```

## Key Concepts

- Project follows the [SOLID](https://en.wikipedia.org/wiki/SOLID) principle as much as possible
- [Swiftlint](https://github.com/realm/SwiftLint) is used to ensure proper styling and convertions are followed
- Project exhibits some amount of Test Coverage

Enjoy! ????
