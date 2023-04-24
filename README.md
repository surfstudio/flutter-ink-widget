# Ink Widget

[![Build Status](https://shields.io/github/actions/workflow/status/surfstudio/flutter-ink-widget/workflow.yaml?logo=github&logoColor=white)](https://github.com/surfstudio/SurfGear/tree/main/packages/ink_widget)
[![Coverage Status](https://img.shields.io/codecov/c/github/surfstudio/SurfGear?flag=ink_widget&logo=codecov&logoColor=white)](https://codecov.io/gh/surfstudio/SurfGear)
[![Pub Version](https://img.shields.io/pub/v/ink_widget?logo=dart&logoColor=white)](https://pub.dev/packages/ink_widget)
[![Pub Likes](https://badgen.net/pub/likes/ink_widget)](https://pub.dev/packages/ink_widget)
[![Pub popularity](https://badgen.net/pub/popularity/ink_widget)](https://pub.dev/packages/ink_widget/score)
![Flutter Platform](https://badgen.net/pub/flutter-platform/ink_widget)

This package made by [Surf](https://surf.ru/).

## Description

Widget library with ink effect without problems with decoration for child.

## Installation

Add ink widget to your `pubspec.yaml` file:

```yaml
dependencies:
  ink_widget: ^2.0.0
```

## Example

```dart
Center(
  child: Column(
    mainAxisAlignment: MainAxisAlignment.center,
    children: <Widget>[
      InkWidget(
        onTap: () {},
        splashColor: Colors.green,
        child: const Text('default InkWidget'),
      ),
      const SizedBox(height: 20),
      InkWidget(
        disable: true,
        onTap: () {},
        child: const Text('disable InkWidget'),
      ),
      const SizedBox(height: 20),
      InkWidget(
        shapeBorder: const RoundedRectangleBorder(
          borderRadius: BorderRadius.all(Radius.circular(20)),
        ),
        onTap: () {},
        child: Container(
          padding: const EdgeInsets.all(10),
          decoration: const BoxDecoration(
            color: Colors.red,
            borderRadius: BorderRadius.all(
              Radius.circular(20),
            ),
          ),
          child: const Text('Container with BoxDecoration'),
        ),
        ),
        const SizedBox(height: 20),
        InkWidget(
          onTap: () {},
          inkWellWidget: InkWell(onTap: () {}),
          child: const Text('Custom InkWell (see code)'),
        ),
        const SizedBox(height: 20),
        InkWidget(
          disable: true,
          onTap: () {},
          disableWidget: Container(
            height: 50,
            color: Colors.white.withOpacity(.2),
            child: const Align(
              alignment: Alignment.bottomLeft,
              child: Text('text in disableWidget'),
            ),
          ),
          child: const Text('Custom disableWidget (see code)'),
        ),
    ],
  ),
),
```

You can use both `stable` and `dev` versions of the package listed above in the badges bar.

## Changelog

All notable changes to this project will be documented in [this file](./CHANGELOG.md).

## Issues

For issues, file directly in the Issues section.

## Contribute

If you would like to contribute to the package (e.g. by improving the documentation, solving a bug or adding a cool new feature), please review our [contribution guide](../../CONTRIBUTING.md) first and send us your pull request.

Your PRs are always welcome.

## How to reach us

Please feel free to ask any questions about this package. Join our community chat on Telegram. We speak English and Russian.

[![Telegram](https://img.shields.io/badge/chat-on%20Telegram-blue.svg)](https://t.me/SurfGear)

## License

[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)
