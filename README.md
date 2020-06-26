# android-sdk-setup

## Description

Install android sdk with specific version

## Inputs

- `ANDROID_COMPILE_SDK`: android sdk version, for example: `28`
- `ANDROID_BUILD_TOOLS`: sdk build tool version, for example: `28.0.2`
- `ANDROID_COMMANDLINE_TOOLS` (optional): commnad tool version, default is `6514223`

## Exports

It will export the flowing envrionment variables to job context

- `ANDROID_HOME`
- `ANDROID_SDK_HOME`

## How to use it

```yml
steps:
- name: setup android sdk
  docker:
    image: openjdk:8-jdk
  envs:
    ANDROID_COMPILE_SDK: "28"
    ANDROID_BUILD_TOOLS: "28.0.2"
  plugin: android-sdk-setup
```
