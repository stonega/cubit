<p align="center"><img src="https://raw.githubusercontent.com/felangel/cubit/master/assets/replay_cubit_full.png" height="100" alt="Cubit"></p>

<p align="center">
<a href="https://pub.dev/packages/replay_cubit"><img src="https://img.shields.io/pub/v/replay_cubit.svg" alt="Pub"></a>
<a href="https://github.com/felangel/cubit/actions"><img src="https://github.com/felangel/cubit/workflows/build/badge.svg" alt="build"></a>
<a href="https://github.com/felangel/cubit/actions"><img src="https://raw.githubusercontent.com/felangel/cubit/master/packages/cubit/coverage_badge.svg" alt="coverage"></a>
<a href="https://github.com/felangel/cubit"><img src="https://img.shields.io/github/stars/felangel/cubit.svg?style=flat&logo=github&colorB=deeppink&label=stars" alt="Star on GitHub"></a>
<a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/license-MIT-purple.svg" alt="License: MIT"></a>
<a href="https://github.com/zepfietje/starware"><img src="https://img.shields.io/badge/Starware-%E2%AD%90-black?labelColor=%23f9b00d" alt="Starware"></a>
</p>

An extension to the [cubit](https://pub.dev/packages/cubit) state management library which adds support for undo and redo.

## Creating a ReplayCubit

```dart
class CounterCubit extends ReplayCubit<int> {
  CounterCubit() : super(0);

  void increment() => emit(state + 1);
}
```

## Using a ReplayCubit

```dart
void main() {
  final cubit = CounterCubit();

  // trigger a state change
  cubit.increment();
  print(cubit.state); // 1

  // undo the change
  cubit.undo();
  print(cubit.state); // 0

  // redo the change
  cubit.redo();
  print(cubit.state); // 1
}
```

## Dart Versions

- Dart 2: >= 2.7.0

## Maintainers

- [Felix Angelov](https://github.com/felangel)

## Starware

ReplayCubit is Starware.  
This means you're free to use the project, as long as you star its GitHub repository.  
Your appreciation makes us grow and glow up. ⭐
