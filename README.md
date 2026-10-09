# Build Your Own Cloud on Windows

Replace Google Photos / Drive-style backup with a server you own, running on
a Windows PC you already have.

A beginner guide built on:

- **Docker Desktop (WSL2)**: runs everything in isolated containers
- **Nextcloud**: the cloud storage app (web, mobile, desktop)
- **Tailscale**: secure remote access with zero open router ports
- **Windows SMB sharing**: fast local file sharing, built in, no Samba needed

Every command runs in PowerShell.

## Read it

**[Open the live guide](https://github.com/kunalchauhan1992/build-NAS-on-windows/windows.html)**

Or open `windows.html` in any browser. It is one self-contained file.
No build step, no dependencies.

## What's inside

- Architecture diagram of how the pieces connect
- Stage-by-stage setup, from WSL2 install to phone photo backup
- Remote access with no port forwarding
- Settings to keep the PC awake and Docker running after reboots
- Security and maintenance checklist
- Troubleshooting table: symptom, real cause
- Full teardown, for starting over

## Windows-specific problems it covers

- Virtualization disabled in BIOS
- Docker Desktop not starting at sign-in
- External drive letter changing after a reboot
- Network profile set to Public, which blocks file sharing
- Windows Update reboots taking the server down
- WSL2 using too much RAM

## Design choice worth knowing

The database lives in a Docker named volume on the internal drive. Only
bulk file storage sits on the external drive. A database on a removable
drive is slow and one unplug away from corruption.

## Know the limits

One PC with one drive is a testing setup, not a backup. Keep a second copy
of anything irreplaceable somewhere physically separate.

This guide has not yet been run end to end on a real Windows machine. Expect
a surprise or two, and open an issue if you hit one.

## Looking for Linux?

A separate Linux edition exists: [link to your Linux repo here]

## Contributing

Found a new dead end, a Windows version where a step differs, or a clearer
explanation? Open an issue or pull request.

## License

MIT. Share freely.
