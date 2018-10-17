# SwiftPM Package Template

<!--{change_me}-->
[![swift-version](https://img.shields.io/badge/Swift-4.2-orange.svg?style=flat)](swift.org)
[![spm](https://img.shields.io/badge/spm-v1.0.0-blue.svg)](https://github.com/apple/swift-package-manager)
[![CocoaPods](https://img.shields.io/cocoapods/v/SwiftEventCenter.svg)](https://cocoapods.org/pods/SwiftEventCenter)
[![Build Status](https://travis-ci.org/ladislas/SwiftEventCenter.svg)](https://travis-ci.org/ladislas/SwiftEventCenter)
[![SonarCloud](https://sonarcloud.io/api/project_badges/measure?project=ladislas_SwiftEventCenter&metric=alert_status)](https://sonarcloud.io/dashboard?id=ladislas_SwiftEventCenter)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=ladislas_SwiftEventCenter&metric=coverage)](https://sonarcloud.io/dashboard?id=ladislas_SwiftEventCenter)
[![SwiftEventCenter](https://img.shields.io/badge/license-Apache--2.0-lightgrey.svg)](https://github.com/ladislas/SwiftEventCenter/blob/master/LICENSE)

<!--{REMOVE EVERYTHING BETWEEN THIS TAG}-->

## About SwiftPM Package Template

**Note:** *Remove this section before publishing your package.*

This repository contains a template directory structure for SPM Library Packages.

### How to use

1. Clone this repository

	```bash
	git clone https://github.com/ladislas/SwiftPM-Package-Template path/to/PackageName
	```

2. `cd` to the cloned repository

	```bash
	cd path/to/PackageName
	```

3. Delete `.git`

	```bash
	rm -rf .git
	```
	
4. Generate your own package with `swift` or [`ice`](https://github.com/jakeheis/Ice)

	```bash
	swift package init
	# or
	ice init
	```
	
5. Reinit `git` and [`git flow`](https://github.com/petervanderdoes/gitflow-avh)

	```bash
	git init
	# and optionally
	git flow init
	```

6. Create your repo on Github and add remote

	```bash
	git remote add origin https://github.com/{user_name}/MyPackage
	```

You're now set up to start developing! 🎉

### What to change - `{change_me}`

This README.md provides you with a the basic information that should present your package's README.md.

#### 

I've added comments and marks using `{change_me}`. Running the following command in your terminal will help you locate & change them:

```bash
ag "{change_me}"
# or
ack "{change_me}"
# or
grep -rnw '.' -e '{change_me}'
```

### Examples

The `Examples` folder is here if you want to provide examples showing how to use your library. Even though documentation and test suites can be helpful resources, it's always a good thing to showcase your library in a "real life" example.

If you want to create an example, just do the following:

```bash
# cd to Examples
cd Examples

# create example directory & cd into it
mkdir MyFirstExample && cd $_

# init example
ice init -e
# or 
swift package init --type executable

# I usually remove the test folder to only keep sources
rm -rf ./Tests
```

Then, for your example to use your library from the local sources and not from a remote repository, add this to your `Package.swift` (change the `PackageName`):

```swift
dependencies: [
    .package(path: "../../../PackageName")
],
```

With this, you can write your examples as your write your library. I really like to be able to immediately use the code. It helps me get a better feeling and can also help with refactoring.

### Documentation

The `docs` folder is used for documentation. If you use [Jazzy](https://github.com/realm/jazzy), you can just run `jazzy` at the root of the project and it will put all documentation to `docs`.

You can then publish it directly on Github. Here are the [instructions](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/#publishing-your-github-pages-site-from-a-docs-folder-on-your-master-branch).

### Travis CI & SonarCloud

If you need continuous integration and code coverage, we got you covered! 

I personally use Travis CI and [SonarCloud](https://sonarcloud.io/). The latter provides you with code coverage and static analysis. And it's super easy to make it works.

To simplify the process & scripting, we are using [IBM's Package-Builder](https://github.com/IBM-Swift/Package-Builder) and providing you with a `.travis.yml` file and a `sonar-project.properties` file.

Steps are:

1. Activate repo on Travis CI
2. Create new project on SonarCloud and generate token
3. Add token to Tracis CI as `SONAR_LOGIN_TOKEN`
4. Enjoy

Detailed instructions on how to use both are available here: 

> [Package-Builder SonarCloud Instructions](https://github.com/IBM-Swift/Package-Builder#sonarcloud)

### Cocoapods

We've also added a `MyProject.podspec` file if you want to publish your library to Cocoapods.

Check [Podspec Syntax Reference](https://guides.cocoapods.org/syntax/podspec.html) and [Marking a CocoaPod](https://guides.cocoapods.org/making/making-a-cocoapod.html) for more information.

### License

This project is under Apache 2.0, but feel free to change the License of your own project. 

### Badges

A lot of badges are present at the top of the README.md. Feel free to keep them or remove them.

If you keep them, you need to change the link they point to with your owns.

---

<!--{AND THIS TAG - REMOVE EVERYTHING}-->

## About

> Describe what your project does. <!--{change_me}-->

### Features

> Describe the main features. <!--{change_me}-->

- [x] - it does this
- [x] - and also this
- [ ] - but not that

## Installation

### Swift Package Manager 

With SPM, add the following to the dependencies of your `Package.swift`

```swift
.package(url: "https://github.com/{change_me}/{change_me}}", from: "1.0.0")
```

### Cocoapods <!--{change_me}-->

You want to add pod 'MyPackage', '~> 1.0' similar to the following to your Podfile:

```ruby
target 'MyApp' do
  pod 'MyPackage', '~> 1.0' 
end
```

Then run a `pod install` inside your terminal.

### Manually

Just copy the [Sources](./Sources) files into your project.

## Usage

> Describe a simple usage <!--{change_me}-->

See [docs](./docs), [Examples](./Examples) & [Tests](./Tests) for more information.

```swift
import MyPackage

let myObj = MyClass()
...
```

## Authors

Made with ❤️ by:

- **{change_me}** - [ladislas](https://github.com/ladislas)

## Contributing 

> Explain how people can contribute to your project <!--{change_me}-->

We welcome contributions, and request you follow these guidelines.

Please raise any bug reports on the issue tracker. Be sure to search the list to see if your issue has already been raised.

A good bug report is one that make it easy for us to understand what you were trying to do and what went wrong. Provide as much context as possible so we can try to recreate the issue.

## License

Apache 2.0 @ Ladislas de Toldi <!--{change_me}-->
