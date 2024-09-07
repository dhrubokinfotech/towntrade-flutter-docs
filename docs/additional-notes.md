# Additional notes

## Static string

For static strings we have user localization. To add a new static string or replace any value, go to the file `/locales/en-US.json`. To add a new string, write a new key and set the string as its value. You can replace a key’s value to replace an existing string. Now run the command:

```
flutter pub run easy_localization:generate \-S "/locales" \-O "lib/locales" \-o "locale_keys.g.dart" \-f keys
```

This will generate a variable inside the file `lib/locales/locale_keys.g.dart`.
In the app, use these generated variables to display a static string.

## public

For asset paths, we are using `flutter_gen_runner`. To activate this package, run these commands on the project’s terminal:

```
dart pub global activate flutter_gen
flutter packages pub run build_runner build
```

If you previously ran the 2nd command, next time use this command to avoid conflict:

```
flutter packages pub run build_runner build \--delete-conflicting-outputs
```

These commands will generate a file `lib/gen/public.gen.dart` and you can use these generated variables for public.
