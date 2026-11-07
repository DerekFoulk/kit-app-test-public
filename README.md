# KitAppTestPublic

Built with [dotnet-agent-kit](https://github.com/DerekFoulk/dotnet-agent-kit) unreleased: its rules, checks and agent instructions apply here. Agents start from `AGENTS.md`.

## Set up a machine

```powershell
./.kit/tools/Initialize-DevMachine.ps1 -RepoRoot .
```

It checks the toolchain (PowerShell 7, Git, GitHub CLI, the .NET SDK in `global.json`) and whether the commit-msg hook is on for this clone. Add `-Install` to install what's missing.

## Build and test

```powershell
dotnet build KitAppTestPublic.slnx
dotnet test --solution KitAppTestPublic.slnx
```

The solution starts empty; the first feature adds its projects.
