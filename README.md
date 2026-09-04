# Mastermind

An iOS recreation of the classic code-breaking game, built with SwiftUI.

The app picks a secret sequence of 4 colors out of 6 possible options. You get 7 guesses to crack it, with feedback after each one telling you how close you were.

## Screenshots

<p float="left">
  <img src="screenshots/gameplay.png" width="260">
  <img src="screenshots/color-picker.png" width="260">
</p>

## How to play

1. Tap a color, then tap one of the four slots in your guess row to place it.
2. Fill all four slots and hit **Enter**.
3. Feedback pegs tell you how close that guess was:
   - a black peg for each correct color in the correct position
   - a white peg for each correct color in the wrong position
4. Crack the code within 7 guesses to win.

## Built with

- SwiftUI for the interface
- `AVFoundation` for background music and sound effects (`Mastermind/backgroundMusic/`)
- [effects-library](https://github.com/GetStream/effects-library) (Swift Package) for the confetti animations on the win/lose screens
- XCTest for unit and UI tests (`MastermindTests/`, `MastermindUITests/`)

## Dependencies

This project pulls in one Swift Package (`effects-library`) directly from GitHub. The first time you open `Mastermind.xcodeproj`, Xcode needs an internet connection to resolve and download it — you'll see a brief "Resolving Package Graph" step before the build works.

## Project structure

```
Mastermind/
├── MastermindApp.swift       entry point, switches between the home/game/tutorial screens
├── ContentView.swift         the main game screen
├── HomePageView.swift        the home screen
├── TutorialView.swift        the how-to-play screen
├── TestButtonView.swift      reusable button component
├── Model.swift                game state and rules
├── ViewModel.swift            connects the model to the views
├── SymbolicConstants.swift    layout and sizing constants
├── backgroundMusic/           music and sound effect playback
└── Assets.xcassets/           images and app icon
```

## Running it

1. Open `Mastermind.xcodeproj` in Xcode.
2. Pick an iOS Simulator (or a connected device) as the run destination.
3. Build and run (`⌘R`).

## Running the tests

`⌘U` in Xcode, or `Product > Test`.

## Author

Ryan Geisler
