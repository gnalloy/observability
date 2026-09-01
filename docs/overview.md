# Overview

[简体中文](overview.zh-CN.md) | [Docs Index](README.md)

## Purpose

Vendor-neutral Gnalloy observability contracts, low-overhead recorders, and Prometheus text export.

This module provides telemetry contracts or adapters. It records bounded metrics and traces without forcing transport, protocol, or vendor-specific dependencies into the core.

## Repository Identity

- Module path: `gnalloy.org/observability`
- GitHub repository: `github.com/gnalloy/observability`
- Default branch: `dev`
- License: Apache-2.0

## Package Map
- `gnalloy.org/observability` (`observability`)

## Direct Gnalloy Dependencies
- `gnalloy.org/gnalloy`

## Direct Dependents in the Current Module Plan
- `gnalloy.org/handler-metrics`
- `gnalloy.org/observability-otel`

## Architecture Position

Gnalloy keeps the core small and dependency-light. This repository is a replaceable module around one responsibility, connected through explicit Go packages instead of runtime discovery.

## Compatibility

The public import path is `gnalloy.org/observability`. Until the first stable tag is published, use `@dev` or an explicit pseudo-version selected by your dependency policy.
