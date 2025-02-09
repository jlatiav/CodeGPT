# Changelog

All notable changes to this project will be documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [2.3.1] - 2024-02-19

### Added

- Support for custom OpenAI model configuration (#250)

### Fixed

- General Settings isModified state
- Azure service credential condition (#375)
- Caret offset location upon document changes (#367)

## [2.3.0] - 2024-02-14

### Added

- Support for autocompletion (disabled by default)
- Support for auto resolving compilation errors

### Replaced

- OpenAI chat models with the most recent ones
- CodeGPT header key

## [2.2.12] - 2023-12-21

### Added

- Support for extended request parameters for llama.cpp

## [2.2.11] - 2023-12-14

### Added

- Support for chatting with multiple files
- Support for generating commit messages and method names with Azure service

## [2.2.10] - 2023-12-12

### Added

- Configurable commit-message system prompt

### Fixed

- Redundant chat tab creation on provider/model change
- Azure bas host and path overriding

## [2.2.9] - 2023-12-04

### Added

- IDE notification on new plugin versions

### Fixed

- LLaMA settings state on server failure

### Improved

- LLaMA server logging

## [2.2.8] - 2023-12-01

### Fixed

- UI concurrency issues (run completion events on EDT)

## [2.2.7] - 2023-11-30

### Fixed

- LLaMA server boot up when additional params are not set

## [2.2.6] - 2023-11-27

### Added

- Support for automatic code formatting (#262)
- Support for additional command-line params for the llama server startup process
- Support for changing between different provides/models in the chat window (#227)
- Deepseek coder instruct models

### Fixed

- Git commit message generation based on the actual user selected/checked files (#291)

### Improved

- Toolwindow Chat UI

## [2.2.5] - 2023-11-23

### Added

- Option to set the number of threads for local LLM models

### Fixed

- Tool window chat editor enabled/disabled logic
- Tool window text pane caret visibility
- Editor actions for `createNewChatOnEachAction` state
- Plugin from crashing when the LLaMA server process is stuck

## [2.2.4] - 2023-11-20

### Added

- Support for git commit message generation
- Support for method/function name lookup generation

### Fixed

- Llama client read/connect timeout configuration

## [2.2.3] - 2023-11-15

### Added

- Expand/Collapse logic for tool window editors
- Interactive total token count label

### Removed

- Azure model selection (redundant field)

## [2.2.2] - 2023-11-07

### Added

- OpenAI GPT-4 Turbo and the latest GPT-3.5 models

### Fixed

- Credential validation when using llama service

## [2.2.1] - 2023-11-06

### Fixed

- Right click context menu (#251)
- Azure path (#232)
- Llama telemetry service value
- Include all feature builds by removing the value (#242)

## [2.2.0] - 2023-11-03

### Added

- Support for running local LLMs via LLaMA C/C++ port (#249)
- Support for fetching You.com subscription

### Fixed

- Project build for Windows ARM64

### Improved

- You.com coupon design
- Overall UI design

## [2.1.7] - 2023-10-26

### Replaced

- You.com GPT-4 toggle component with checkbox
- Telemetry segment service with rudderstack

### Fixed

- You.com web search not being displayed regardless of the flag

## [2.1.6] - 2023-10-12

### Added

- Default destination value for toolwindow editor save file action
- Suggestion to switch to different LLM provider on quota exceeded error
- Support for You.com GPT-4 model

### Fixed

- The style of wrapping used if the text area is wrapping lines
- Memory leaks (correct disposals for Configurable classes)

## [2.1.5] - 2023-10-02

### Added

- Support for diffing generated code

## [2.1.4] - 2023-10-01

### Added

- Support for modifying generated code within the chat toolwindow
- Support for creating new files directly from the chat toolwindow 

### Fixed

- Privacy policy url in the settings

## [2.1.3] - 2023-09-28

### Added

- More telemetry actions

### Fixed

- Error logging

## [2.1.2] - 2023-09-28

### Fixed

- Incorrect window selection during chat or toolwindow actions

## [2.1.1] - 2023-09-27

### Added

- Telemetry based on redhat impl

## [2.1.0] - 2023-09-21

### Added

- You API integration
- Ability to override completion path

### Updated

- Chat History UI

## [2.0.6] - 2023-08-29

### Removed

- Functionality to fetch/use OpenAI account name

### Fixed

- Rendering user input's newlines

### Added

- Support for closing other tabs (#172)
- Support for configuring custom hosts for OpenAI and Azure services

## [2.0.5] - 2023-06-12

### Fixed

- Tool window not opening on editor actions (#157)

### Added

- Support for changing the editor action behaviour (#157)
- Support for overriding completions request parameters (#152)
- User text area autofocus on creating a new chat (#155)
- Keymap tool window actions (#148)

## [2.0.4] - 2023-05-27

### Fixed

- TypeScript and C# code highlighting

- ToolWindow usability when virtual space option turned ON (#125) 

### Added

- ToolWindow code editor copy/replace header actions
- Custom prompt main editor action (#144)
- Support for 2023.2 EAP builds (#149)

## [2.0.3] - 2023-05-18

### Fixed

- Empty editor context menu item text (#137)
- Temp file path resolving (#130)

### Improved

- Response streaming

### Added

- Reset chat window toolbar action (#138)

## [2.0.2] - 2023-05-16

### Fixed

- Settings deserialization error

### Improved

- Memory consumption by disposing unused editors which are no longer needed

### Removed

- Main editor focus stealing on response streaming

## [2.0.1] - 2023-05-14

### Added

- New GPT-3.5-16k model 

### Fixed

- NPE when `displayName` couldn't be fetched

### Improved

- Proxy support by disabling the default trustmanager

### Removed

- Off-screen rendering setting option
- Automatic textarea focus on stream completion (#126)

## [2.0.0] - 2023-05-03

### Added

- Automatic retry logic on stream timeouts

### Improved

- Input prompt text field UI/UX (height grows with the content)

### Removed

- Custom prompt editor action (users can now provide custom actions within the chat window itself)

### Replaced

- ToolWindow HTML content with native Swing components

### Secured

- `OPENAI_API_KEY` persistence, key is saved in the OS password safe from now on

[Unreleased]: https://github.com/carlrobertoh/CodeGPT/compare/v2.3.1...HEAD
[2.3.1]: https://github.com/carlrobertoh/CodeGPT/compare/v2.3.0...v2.3.1
[2.3.0]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.12...v2.3.0
[2.2.12]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.11...v2.2.12
[2.2.11]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.10...v2.2.11
[2.2.10]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.9...v2.2.10
[2.2.9]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.8...v2.2.9
[2.2.8]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.7...v2.2.8
[2.2.7]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.6...v2.2.7
[2.2.6]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.5...v2.2.6
[2.2.5]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.4...v2.2.5
[2.2.4]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.3...v2.2.4
[2.2.3]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.2...v2.2.3
[2.2.2]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.1...v2.2.2
[2.2.1]: https://github.com/carlrobertoh/CodeGPT/compare/v2.2.0...v2.2.1
[2.2.0]: https://github.com/carlrobertoh/CodeGPT/compare/v2.1.7...v2.2.0
[2.1.7]: https://github.com/carlrobertoh/CodeGPT/compare/v2.1.6...v2.1.7
[2.1.6]: https://github.com/carlrobertoh/CodeGPT/compare/v2.1.5...v2.1.6
[2.1.5]: https://github.com/carlrobertoh/CodeGPT/compare/v2.1.4...v2.1.5
[2.1.4]: https://github.com/carlrobertoh/CodeGPT/compare/v2.1.3...v2.1.4
[2.1.3]: https://github.com/carlrobertoh/CodeGPT/compare/v2.1.2...v2.1.3
[2.1.2]: https://github.com/carlrobertoh/CodeGPT/compare/v2.1.1...v2.1.2
[2.1.1]: https://github.com/carlrobertoh/CodeGPT/compare/v2.1.0...v2.1.1
[2.1.0]: https://github.com/carlrobertoh/CodeGPT/compare/v2.0.6...v2.1.0
[2.0.6]: https://github.com/carlrobertoh/CodeGPT/compare/v2.0.5...v2.0.6
[2.0.5]: https://github.com/carlrobertoh/CodeGPT/compare/v2.0.4...v2.0.5
[2.0.4]: https://github.com/carlrobertoh/CodeGPT/compare/v2.0.3...v2.0.4
[2.0.3]: https://github.com/carlrobertoh/CodeGPT/compare/v2.0.2...v2.0.3
[2.0.2]: https://github.com/carlrobertoh/CodeGPT/compare/v2.0.1...v2.0.2
[2.0.1]: https://github.com/carlrobertoh/CodeGPT/commits/v2.0.1
[2.0.0]: https://github.com/carlrobertoh/CodeGPT/commits/v2.0.0
