# Versioning
## Why do we need versioning for the *Cocoa App*

>Before getting to the when and how, let’s start with why. My main aims are that:
>- Everyone should know what features are available in the version of the app they have
>- Everyone should know what version of the app they have if they are reporting bugs or requesting support  
>
>When I say everyone, I mean anyone who uses your app, including internal testers, beta testers and end users.

That is the reasoning from [Gabrielle Earnshaw](https://medium.com/@GabEarnsh/versioning-mobile-app-releases-like-a-pro-25137766150a). And the same reasoning applies to the *Cocoa App*, to make it easier to reference our app version than to use git-hashes.  

## How should a version number look like

I would suggest a similar approch like described by Gabrielle Earnshaw. We have 3 number brackets seperated by dots: `major.minor.patch`.
- `major` is for major changes, for example v.1.0.0 for the release of the full app.
- `minor` for additional functionalites, like the ability to see the robot or to import robots.
- `patches` for minor changes or bugfixes

If you increment a higher component, you zero out the lower ones, so `1.2.13` would become `1.2.14` with a patch version increase, `1.3.0` with a minor version increase and `2.0.0` with a major version increases.

## Other strategies and their disadvantages
- **Commit hashes**: This uniquely identifies the release, but gives you no information about the order in which the releases occurred. For example if you have a feature that was added in version `1.3.4` and you have version `1.4.1`, you know it is included. However if it was added in version `9a10ea01`, you have absolutely no idea if it should be available or not in version `13be2fc4`.
- **No versioning**: An developer who tests something and wonders why it doesn't work, when it should be, will be something that will happen without versioning.

# Example Roadmap/Versioning for the Cocoa App
