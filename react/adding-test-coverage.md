# Adding test coverage to React

In the package.json file, we need to add two arguments to the test script:

- `--coverage`: Turns on the test coverage stats included in Jest

- `--watchAll=false`: turns off the watcher which reruns the test suite whenever they are updated.

Before:

```json

 "test": "react-scripts test"
```

After:

```json

 "test": "react-scripts test --coverage --watchAll=false"
```

We also need to add some configurations for jest, where we can define the file patterns to include in coverage, files to ignore and the minimum coverage percentage. Below are some standard settings that can be added to the package.json file.

```json

"jest": {
    "collectCoverageFrom": [
      "src/**/*.{js,jsx,ts,tsx}",
      "!src/index.js",
      "!<rootDir>/node_modules/",
      "!<rootDir>/path/to/dir/"
    ],
    "coverageThreshold": {
      "global": {
        "branches": 90,
        "functions": 90,
        "lines": 90,
        "statements": 90
      }
    }
  }
```

[Main Page](../README.md)
