Source: https://learn.microsoft.com/en-us/events/dotnetconf-2022/testing-blazor-applications-with-playwright

- supported for any platform, any browser
- supported for many languages e.g. node and blazor
- single api to rule them all

- tests are run in isolation, no bleed from one test into another
- playwright uses in memory browser context to quickly test as opposed to restarting a browser each time

## Autowaiting concepted
- instead of clicking button
    - PR doe extra steps
    - e.g. making sure element visible, stable, clickable, enabled
    - does this until a timeout is reached

## Code gen
- allows you to set up tests by clicking through the interface
- automatically figures out which selectors to use

## Playwright tracing
- debugging tests
- lists all steps that got performed in a timeline
- will give you a snapshot of the site so you can debug with dev tools

## Donet and Playwrite
- you can use it as a library in tests
- can also be built into pipelines
- installing dotnet pakage Microsoft.Playwright.MSTest
    - installs playright and the integration
    - doesn't install browsers by default
    - need to install it by using the Playwright script in the debug folder of the solution
- can use PauseAsync to pause the unit test with debugging

## Code gen
run playwright.ps1 codegen <Website URL>

## Running on CI
https://github.com/mxschmitt/DotnetConfDemoTest0947
