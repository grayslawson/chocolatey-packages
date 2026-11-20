# Chocolatey feed for Osprey

Osprey is the Ubiquiti PTZ controller for an existing Frigate installation.

```powershell
choco install osprey --source https://github.com/grayslawson/chocolatey-packages
```

The package installs the release compose file under
`C:\ProgramData\osprey\compose.release.yaml`. It does not pull the image and
does not start anything: set the camera address and MAC in the compose file,
then run `docker compose -f <file> up -d`.

Packages are built from the latest published Osprey release by a scheduled
workflow. The source of truth is the
[Osprey repository](https://github.com/grayslawson/osprey).
