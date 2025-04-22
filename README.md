# Woohoo.Platform.Windows

![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/huguesv/PlatformWindows/build-and-test.yml)
![NuGet Version](https://img.shields.io/nuget/v/Woohoo.Platform.Windows)

Library of Windows-only platform APIs for .NET

## Taskbar

Use `TaskbarManager` to manage the taskbar progress bar.

```csharp
using Woohoo.Platform.Windows.Taskbar;

TaskbarManager.Instance.SetProgressValue(10, 100);

TaskbarManager.Instance.SetProgressState(TaskbarProgressBarState.Normal);
```

## Power Management

Use `ThreadExecutionManager` to manage power settings.

```csharp
using Woohoo.Platform.Windows.PowerManagement;

// Prevent the system from sleeping
ThreadExecutionManager.SetState(ThreadExecutionState.Continuous | ThreadExecutionState.DisplayRequired);

// Restore sleep settings
ThreadExecutionManager.SetState(ThreadExecutionState.Continuous);
```
