# Expo Web: Cryptic Webpack Errors with Custom Configuration

This repository demonstrates a bug encountered when using Expo Web with a custom webpack configuration. The issue leads to cryptic error messages during the build process, often related to module resolution despite correctly installed dependencies. The root cause is a conflict between Expo's internal webpack setup and the custom configuration.

## Bug Description

When attempting to integrate a custom webpack configuration with Expo Web, the build process fails with confusing and unhelpful error messages.  The errors often suggest missing modules or unresolved paths, even though `npm install` or `yarn install` have successfully installed all necessary dependencies.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Attempt to start the Expo Web project using `expo start --web`.
4. Observe the cryptic webpack error messages.

## Solution

The solution involves carefully merging the necessary parts of the custom webpack configuration with Expo's default configuration, avoiding conflicts.  This often requires a deep understanding of both webpack and Expo's internal workings.  See `bugSolution.js` for a potential fix.