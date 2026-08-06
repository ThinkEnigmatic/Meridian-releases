# Meridian — Downloads

**Meridian** is a private, local-first household financial command center. All your data stays
encrypted on your own machine — nothing is uploaded anywhere.

> This repository hosts the **installers only**. The source code is private.

## Install

Grab the latest installer for your operating system from the
[**Releases**](https://github.com/ThinkEnigmatic/Meridian-releases/releases/latest) page:

- **macOS** (Apple Silicon or Intel): download the `.dmg`, open it, drag **Meridian** to Applications.
- **Windows** (64-bit): download the `-setup.exe` and run it.

Once installed, Meridian keeps itself up to date automatically — you won't need to download again.

## First launch (the app is not code-signed yet)

Because the app isn't signed with a paid developer certificate, your OS will warn you the first time:

- **macOS:** right-click **Meridian** → **Open** → **Open**. If it still refuses ("damaged / can't be
  opened"), run once in Terminal: `xattr -dr com.apple.quarantine /Applications/Meridian.app`
- **Windows:** on the SmartScreen prompt, click **More info** → **Run anyway**.

This is a one-time step per install; updates apply silently after that.

## Setting up

On first run you'll pick a name, set **your own password**, and either start solo or create/join a
household. Household members sync through a shared cloud folder and are linked by a one-time invite
code — there is never a shared password.
