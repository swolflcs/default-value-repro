# Reproduction

1. Run `npm run storybook`
2. Open brower console to see error

# Bug Report

**Describe the bug**
After creating a new angular project, running `npx sb init`, and then starting storybook the following deprecation message appears in the browser console:

```
`argType.defaultValue` is deprecated and will be removed in Storybook 7.0.
```

**To Reproduce**
1. I created a reproduction by running `npx sb@next repro` and selecting framework angular/angular ([repository](https://github.com/swolflcs/default-value-repro))
2. Run storybook with `npm run storybook` without making changes
3. Open console to view error

https://github.com/swolflcs/default-value-repro

**System**

```
  System:
    OS: Windows 10 10.0.19042
    CPU: (16) x64 Intel(R) Core(TM) i7-10700 CPU @ 2.90GHz
  Binaries:
    Node: 14.17.5 - C:\Program Files\nodejs\node.EXE
    Yarn: 3.0.2 - ~\AppData\Roaming\npm\yarn.CMD
    npm: 6.14.14 - C:\Program Files\nodejs\npm.CMD
  Browsers:
    Edge: Spartan (44.19041.1023.0), Chromium (93.0.961.38)
  npmPackages:
    @storybook/addon-actions: ^6.4.0-alpha.34 => 6.4.0-alpha.34
    @storybook/addon-docs: ^6.4.0-alpha.34 => 6.4.0-alpha.34
    @storybook/addon-essentials: ^6.4.0-alpha.34 => 6.4.0-alpha.34
    @storybook/addon-links: ^6.4.0-alpha.34 => 6.4.0-alpha.34
    @storybook/angular: ^6.4.0-alpha.34 => 6.4.0-alpha.34
    @storybook/builder-webpack5: ^6.4.0-alpha.34 => 6.4.0-alpha.34
    @storybook/manager-webpack5: ^6.4.0-alpha.34 => 6.4.0-alpha.34
```

**Additional context**

- This issue was discovered as a part of a large storybook project I was working on. I removed all of the uses of argType.defaultValue in the project and was still getting this deprecation error.
- For some reason in my reproduction repository I am unable to get the project to load in chrome. If this happens to you, I was able to load the project in Firefox. I made no changes in my reproduction so it is either my machine or another bug. I don't have the time to investigate that right now though.