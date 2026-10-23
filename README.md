# doromiert’s ZenOS Next config

In the new ZenOS installer, choose **Online config**, enter
`github:doromiert/zenos-next-config`, select **doromi-tul-2**, then enter
**doromiert** and your new password.

This configuration declares only doromiert. It includes GNOME, the legacy
creative/development applications, Docker/Libvirt, Steam/ALVR/VR overlays,
printer and Logitech support, current Codex CLI/Desktop, Jupiter and Select for
Figma. ZeroBridge is omitted. System and user Flatpaks retain their scopes.
Yuzu uses the cached NixOS 23.11 package instead of the discontinued Flatpak.

Setup replaces `hardware.zcfg`, `graphics.zcfg`, and `drives.zcfg` with the new
machine’s hardware and the partitions selected in the installer. The committed
files are empty placeholders; no old disk UUIDs or password hashes are included.
The config retains the AMD/Zen kernel policy of doromi-tul-2, so it is intended
for that machine. Setup validates it before partitioning.

Back up personal data separately: passwords, browser profiles, Steam libraries,
VR settings, virtual machine disks, Flatpak data, and projects are not stored in
this repository. The account home is `/Users/doromiert`, with managed XDG data
under `.private`, as required by ZenOS Next. State version remains `25.11`.

Use an ISO containing the online-install runner implementation; older images
show the online-config page but reject the installation.
