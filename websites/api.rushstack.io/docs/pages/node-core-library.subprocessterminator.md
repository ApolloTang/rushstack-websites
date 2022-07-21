---
hide_title: true
custom_edit_url: null
pagination_prev: null
pagination_next: null
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@rushstack/node-core-library](./node-core-library.md) &gt; [SubprocessTerminator](./node-core-library.subprocessterminator.md)

## SubprocessTerminator class

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.

When a child process is created, registering it with the SubprocessTerminator will ensure that the child gets terminated when the current process terminates.

<b>Signature:</b>

```typescript
export declare class SubprocessTerminator
```

## Remarks

This works by hooking the current process's events for SIGTERM/SIGINT/exit, and ensuring the child process gets terminated in those cases.

SubprocessTerminator doesn't do anything on Windows, since by default Windows automatically terminates child processes when their parent is terminated.

## Properties

| Property                                                                               | Modifiers                                              | Type                                                            | Description                                                                 |
| -------------------------------------------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------- | --------------------------------------------------------------------------- |
| [RECOMMENDED_OPTIONS](./node-core-library.subprocessterminator.recommended_options.md) | <p><code>readonly</code></p><p><code>static</code></p> | [ISubprocessOptions](./node-core-library.isubprocessoptions.md) | <b><i>(BETA)</i></b> The recommended options when creating a child process. |

## Methods

| Method                                                                                                                    | Modifiers           | Description                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| [killProcessTree(subprocess, subprocessOptions)](./node-core-library.subprocessterminator.killprocesstree.md)             | <code>static</code> | <b><i>(BETA)</i></b> Terminate the child process and all of its children.                                                        |
| [killProcessTreeOnExit(subprocess, subprocessOptions)](./node-core-library.subprocessterminator.killprocesstreeonexit.md) | <code>static</code> | <b><i>(BETA)</i></b> Registers a child process so that it will be terminated automatically if the current process is terminated. |