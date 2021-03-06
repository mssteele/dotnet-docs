---
title: Diagnostics tools overview - .NET Core
description: An overview of the tools and techniques available to diagnose .NET Core applications.
author: sdmaclea
ms.author: stmaclea
ms.date: 10/14/2019
ms.topic: overview
#Customer intent: As a .NET Core developer I want to find the best tools to help me diagnose problems so that I can be productive.
---
# What diagnostic tools are available in .NET Core?

Software doesn't always behave as you would expect, but .NET Core has tools and APIs that will help you diagnose these issues quickly and effectively.

This article helps you find the various tools you need.

## Managed debuggers

[Managed debuggers](managed-debuggers.md) allow you to interact with your program. Pausing, incrementally executing, examining,  and resuming gives you insight into the behavior of your code. A debugger is the first choice for diagnosing functional problems that can be easily reproduced.

## Logging and tracing

[Logging and tracing](logging-tracing.md) are related techniques. They refer to instrumenting code to create log files. The files record the details of what a program does. These details can be used to diagnose the most complex problems. When combined with time stamps, these techniques are also valuable in performance investigations.

## Unit testing

[Unit testing](../testing/index.md) is a key component of continuous integration and deployment of high-quality software. Unit tests are designed to give you an early warning when you break something.

## .NET Core dotnet diagnostic Global Tools

### dotnet-counters

[dotnet-counters](dotnet-counters.md) is a performance monitoring tool for first-level health monitoring and performance investigation. It observes performance counter values published via the <xref:System.Diagnostics.Tracing.EventCounter> API. For example, you can quickly monitor things like the CPU usage or the rate of exceptions being thrown in your .NET Core application.

### dotnet-dump

The [dotnet-dump](dotnet-dump.md) tool is a way to collect and analyze Windows and Linux core dumps without a native debugger.

### dotnet-trace

.NET Core includes what is called the `EventPipe` through which diagnostics data is exposed. The [dotnet-trace](dotnet-trace.md) tool allows you to consume interesting profiling data from your app that can help in scenarios where you need to root cause apps running slow.
