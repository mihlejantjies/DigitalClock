# DigitalClock

# Digital Clock (C# Console App)

A simple digital clock for beginners, written in C#. It shows the current time and date in the console and updates every second.

## Features

- Displays the time in 24-hour format (`HH:mm:ss`)
- Displays the full date (e.g. `Wednesday, 18 November 2026`)
- Updates in place every second (no scrolling)
- Press any key to exit

## Requirements

- [Visual Studio 2022](https://visualstudio.microsoft.com/) with the **.NET desktop development** workload, or
- The [.NET SDK](https://dotnet.microsoft.com/download) (if using the command line)

## Getting Started

### Option 1: Visual Studio

1. Open Visual Studio and click **Create a new project**.
2. Choose **Console App** (C#, not .NET Framework) and click **Next**.
3. Name the project `DigitalClock` and click **Next**, then **Create**.
4. Open `Program.cs`, select everything (**Ctrl+A**), delete it, and paste in the code from this project.
5. Press **Ctrl+F5** (Start Without Debugging) to run.

### Option 2: Command line

```bash
dotnet new console -n DigitalClock
cd DigitalClock
# replace Program.cs with the one from this project
dotnet run
```

## How It Works

| Code | Purpose |
|------|---------|
| `DateTime.Now` | Gets the current local date and time |
| `ToString("HH:mm:ss")` | Formats the time as a 24-hour clock |
| `Console.SetCursorPosition` | Moves back to the same line so the clock updates in place |
| `Thread.Sleep(1000)` | Waits one second between updates |
| `Console.KeyAvailable` | Lets the loop end when a key is pressed |

## Customising

- **12-hour clock:** change `"HH:mm:ss"` to `"hh:mm:ss tt"`.
- **Date format:** change `"dddd, dd MMMM yyyy"` to any format you like, e.g. `"yyyy-MM-dd"`.

## Troubleshooting

- **Duplicate `Main` error:** the original starter code is still in `Program.cs`. Delete all of it before pasting.
- **Console window closes immediately:** run with **Ctrl+F5**, not F5.
- **Clock prints repeatedly down the screen:** the console window is too small; enlarge it.

## Next Steps

- Add colours with `Console.ForegroundColor`
- Add a 12/24-hour toggle
- Build a windowed version with WPF and a `DispatcherTimer`
