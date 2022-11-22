# Reusable CI jobs
This is a repository that is only interesting to those who want to understand the whole inner workings of how the homeworks are checked. This repository contains CI jobs (using GitHub Actions) that handle:
- Checking out the repositories with:
  - Homeworks (created from the [homeworks](https://github.com/cpp-for-yourself/homeworks) template)
  - Homework definitions (from [this](https://github.com/cpp-for-yourself/homework-definitions) repository)
- Installing software:
  - Different python dependencies
  - The [homework-checker](pip install homework-checker) from `pip`
- Creating and updating comments in a PR
- Actually running the homework checker on the user-provided code.

The jobs in this repo are meant to be (re)used from the [homeworks](https://github.com/cpp-for-yourself/homeworks) template repository and from the repositories created from it.

## Why does this exist
Just like in normal code it is nice to decouple code and to reuse the logic. Here what I wanted to achieve is to be able to change the way the jobs run for all the people that created their projects from the [homeworks](https://github.com/cpp-for-yourself/homeworks) template. Currently, once the projects are created from that template, I have no control over the CI in those projects. That means, if I missed something in the original CI job, there is no way to fix it for me anymore.

With the reusable jobs here I can change this reusable job and fix the pipelines should they be broken for everybody who already created their repositories from the template earlier.
