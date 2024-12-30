# Simple Interpreter for Learning Jenkins and CI/CD
 
A simple interpreter writing in OCaml and testing in Jenkins

## Overview

A lightweight interpreter that can parse and interp simple expressions. Also for the purpose of learning and using of Jenkins.


## Environment

- OCaml, Opam, OUnit2, Dune
- Windows 10+, Linux or macOS.

## Deployment

1. Build project: dune utop
2. Run tests: dune runtest
3. Clean cache: dune clean


## Jenkins

- The main purpose of this project is learning and testing in Jenkins pipeline for CI/CD study.
- A Jenkinsfile has been set up to run tests, build the project, and deploy it automatically in Jenkins pipeline.


## Credit

- Reference: [PLaF](https://github.com/ebonelli/PLaF)
