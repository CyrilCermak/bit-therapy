# BitTherapy (Desktop Pets)
This is the source code of my macOS app [BitTherapy](https://apps.apple.com/app/desktop-pets/id1575542220)!.

As you can guess, it brings Desktop Pets to macOS 🚀

Like the app? Join our [Discord](https://discord.gg/MCdEgXKSH5)!

## 🎮 Supported Systems
The app is currently available for macOS only via the [App Store](https://apps.apple.com/app/id1575542220).

Is this coming to Windows or Linux? Yes... But... Hear me out...

I'm currently using this project to learn a bit more about [Rust](https://github.com/curzel-it/pet-therapy/tree/main/Sources/rust/README.md) and [C++](https://github.com/curzel-it/pet-therapy/tree/main/Sources/cpp/README.md), I'm actively working on both ports.

Previously, I've also started working on a [Python/QT](https://github.com/curzel-it/pet-therapy/tree/main/Sources/python/README.md) port of the app, but to be honest, it's been quite boring and I will likely never touch it again.

## 🤔 What's a Desktop Pet?
It's just a cute little pet or animal that lives in your computer.

The most popular one was probably the [eSheep](https://github.com/Adrianotiger/desktopPet) for Windows 95.

Hope you like them too!

## 📲 Get the app
For daily use I recommend getting the App from the App Store.

Alternatively, you can download the latest release from [GitHub]( https://github.com/curzel-it/pet-therapy/releases/latest) or build from source (see below).

[![Get it on the App Store](docs/appstore_badge.png)](https://apps.apple.com/app/id1575542220)

## 🔥 Screenshots
![Homepage, light mode](docs/1.png)
![Settings, dark mode](docs/2.png)

## 🎨 Create custom pets
Starting from version 2.20 you can now create custom pets, please check [the documentation](https://curzel.it/pet-therapy/custompets).

You do not need any programming knowledge or Xcode to create your own pets, just design your characters and follow [the instructions](https://curzel.it/pet-therapy/custompets), good luck!

## 🙏 Contribute
Contributors get a shout out in the app, just saying... 😏
![Contributors, dark mode](docs/contributors.png)

If you wish to improve support for your language, join our [Discord](https://discord.gg/MCdEgXKSH5) and let us know!

## 🔔 Interoperability
Since version 2.48 you can use `DistributedNotificationCenter` to send basic commands to your pets.

Here's the payload:

```json
{
    # Species id
    "subject": "sloth",
    
    # Animation id
    "action": "eat",
    
    # Optional, both x and y required 
    "x": 100,
    "y": 100
}
```

Sample Python script to send out notifications:
```python
from Foundation import NSDistributedNotificationCenter, NSDictionary

def send_notification():
    notification_name = "it.curzel.pets.Api"
    message = {...}
    user_info = NSDictionary.dictionaryWithDictionary_(message)
    center = NSDistributedNotificationCenter.defaultCenter()
    center.postNotificationName_object_userInfo_deliverImmediately_(
        notification_name, None, user_info, True
    )

if __name__ == "__main__":
    send_notification()
```

## 🛠️ Build from Source
1. Download and setup Xcode
1. Open the `Sources/swift/BitTherapy.xcworkspace`
1. Give Xcode some time to figure out dependencies...
1. Run

## About me
I have a [YouTube Channel](https://www.youtube.com/@HiddenMugs) which has been gathering lots of dust lately.
