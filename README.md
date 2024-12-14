# Expo CLI: Uncommon Build Errors and Dependency Conflicts

This repository demonstrates an uncommon bug encountered when using the Expo CLI, specifically concerning dependency conflicts and issues with EAS Build.  The bug manifests as unexpected build failures and runtime crashes during development.

## Bug Description

The primary issue arises from mismatched versions of Expo SDK, React Native, and other dependencies.  This often occurs when updating packages independently without considering version compatibility.  Incorrectly configured EAS Build settings (e.g., specifying incompatible SDK versions) can further exacerbate these problems.

## Bug Reproduction

The `expoBug.js` file contains a simplified example that highlights dependency issues. To reproduce, you might need to manually introduce version conflicts or misconfigurations in your `package.json` and EAS Build configuration.

## Solution

The `expoBugSolution.js` file presents a solution focusing on careful dependency management and correctly configuring EAS Build. Key steps include:

1.  **Using Expo's version management tools:** Ensure that React Native and Expo SDK versions are compatible by following Expo's guidelines.  `expo upgrade` can help.
2.  **Resolving version conflicts:** Use tools like `npm-check-updates` to identify outdated packages and carefully manage versions using semantic versioning to avoid breaking changes.
3.  **Proper EAS Build configuration:** Carefully check and validate your EAS Build configuration file (`eas.json`), verifying that the specified SDK and other build settings are compatible with your project's dependencies.
4.  **Clean rebuilds:** Often, a clean rebuild (`expo start --reset-cache`) helps clear out stale cached build artifacts.

## Contributing

Contributions are welcome!  If you have encountered similar problems or have additional solutions, please feel free to open an issue or submit a pull request.