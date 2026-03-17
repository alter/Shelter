2.0 (WIP)
===

### Android 16 / OxygenOS 16 support
- Updated targetSDK to 36 (Android 16) for OxygenOS 16 / OnePlus 12 compatibility.
- Fixed Intent redirection hardening and scoped storage permissions for Android 16.

### Security fixes
- Fixed path traversal vulnerability in file handling.
- Fixed memory leaks and improved sandbox hardening.

### Dependency updates
- Updated Gradle to 8.11.1, AGP to 8.7.3.
- Bumped appcompat to 1.7.1, test runner to 1.7.0, espresso to 3.7.0.
- Replaced deprecated `LocalBroadcastManager` with `LiveData`.
- Added missing `androidx.swiperefreshlayout` dependency.

### New features
- Per-app permission blocking for location and contacts in the work profile.

### Build & infrastructure
- Added Docker build environment for reproducible Android builds.
- Included self-signed release keystore in the repo for out-of-the-box signed builds.
- Fixed multiple Docker build issues (git safe.directory, submodule init, submodule URL migration to GitHub).

1.9.1 (445)
===

- Hotfix crashes below Android 11.

1.9
===

- Updated targetSDK to 34 (Android 14) with compatibility fixes.
- More reliable delayed freezing using AlarmManager (thanks parmaster84).
- Support for cross-profile interactions allowlisting (e.g. for Gboard).
- Removed "Fake Camera" feature as it has not been supported since R.
- Version displayed within the app has now been changed to also reflect the exact Git commit when the app is built.
- File Shuttle no longer appends ".null" or ".bin" suffixes unnecessarily. This should make it work much better with file managers such as Material Files.
- File Shuttle now triggers media scanning much more robustly. Media files (pictures, videos, etc.) copied into the work profile should now show up much quicker in gallery apps.
- Added a fake NFC payment service to workaround a bug in Android that prevents payment apps inside the work profile from being used if none is present in the main profile.
- Fixed unintuitive colors of navigation icons under dark mode.

1.8
===

- Updated targetSDK to 33 (Android 13) with compatibility fixes.
- UI style revamp with Material You support on Android 12+.

1.7
===

- Revamped the initial setup process to include a full setup guide for better clarity and less confusion.
- Upgraded targetSDK to 31 (Android 12) with compatibility fixes.
- Upgraded dependencies.
- Translation updates thanks to our wonderful community.

1.6
===

- Start of in-repo changelogs
- Add support for Android 11 (c147377, 3852bd, and more) (__Note__: For now, File Shuttle is not available in the version on Google Play due to policy reasons, as they will not be allowing apps with All Files permission before 2021.)
- Shelter can no longer be installed to external storage (removable SD cards) (9a6777 by Camilio Alejo)
- Allow more browsable intents to be passed across work / main profile boundary (43444b by Camilio Alejo)
- A new shortcut to Documents UI is available in the three-dot menu of Shelter, because on Pixels the Google Files app may not be able to open File Shuttle correctly (a121ee)
- You can now choose to block or allow cross-profile contact access via a settings option (749ad1)
- Thanks to translators participating in our Weblate instance (https://weblate.typeblog.net), Shelter is now available in more languages. You can now contribute translations easier than ever by using the Weblate interface.
