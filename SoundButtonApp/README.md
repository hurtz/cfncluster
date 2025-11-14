# Sound Button App

A simple iOS app with a button that plays a sound when pressed.

## Features

- Clean, modern SwiftUI interface
- Beautiful gradient button design
- Plays a system beep sound when tapped
- Haptic feedback for better user experience
- Works on both iPhone and iPad

## Requirements

- iOS 15.0 or later
- Xcode 14.0 or later
- macOS with Xcode installed

## How to Run

1. Open `SoundButtonApp.xcodeproj` in Xcode
2. Select a simulator or connect your iOS device
3. Click the Run button (or press Cmd+R)
4. Tap the "Play Sound" button to hear the sound

## Project Structure

```
SoundButtonApp/
├── SoundButtonApp.xcodeproj/
│   └── project.pbxproj
└── SoundButtonApp/
    ├── SoundButtonAppApp.swift    # App entry point
    ├── ContentView.swift           # Main UI with button
    ├── Assets.xcassets/            # App icons and assets
    └── Info.plist                  # App configuration
```

## How It Works

The app uses:
- **SwiftUI** for the user interface
- **AudioServicesPlaySystemSound** to play a system beep sound (ID: 1104)
- **UIImpactFeedbackGenerator** for haptic feedback when the button is tapped

## Customization

You can modify the sound by changing the system sound ID in `ContentView.swift`:

```swift
AudioServicesPlaySystemSound(1104) // Change this number to try different system sounds
```

Common system sound IDs:
- 1103: Texttone (Alert)
- 1104: SMS Alert
- 1105: Alarm
- 1107: Anticipate

You can also add your own audio files and use AVAudioPlayer for more control over playback.
