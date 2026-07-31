# MacMine

MacMine is a native SwiftUI macOS menu-bar app for creating and managing local Minecraft server folders. Its app icon is a simple green cube mark on a pale rounded macOS-style background.

Developer: Morten Buus

MacMine is an unofficial Minecraft server management tool. It is not affiliated with, endorsed by, sponsored by, or approved by Microsoft, Mojang, Canonical, PaperMC, FabricMC, Minecraft Forge, SpigotMC, Bukkit, SpongePowered, Eclipse Adoptium, or Apple.

## What It Does

MacMine provides a simple macOS interface for:

- Creating local Minecraft server profiles.
- Choosing Bedrock, Vanilla, CraftBukkit, Spigot, Paper, Fabric, Forge, or Sponge.
- Downloading/preparing server packages from official or user-configured sources.
- Applying common server settings.
- Scaling the main dashboard for better screen space.
- Warning when a selected port is already in use, including the running MacMine server name when known.
- Starting, stopping, and restarting servers.
- Viewing selectable console output.
- Tracking players and running common player commands.
- Importing, enabling, and disabling plugin/mod `.jar` files.
- Checking for updates, postponing updates, skipping versions, and cancelling active update work.
- Running Bedrock's Linux server package through Canonical Multipass.
- Forwarding Bedrock UDP traffic from the Mac to the Multipass VM.
- Exporting/importing text-based `.macmine` server descriptions.

## Important Legal Notes

MacMine does not include Minecraft, Minecraft server binaries, plugin jars, Multipass, Java, or Ubuntu in the app bundle.

MacMine downloads or opens third-party packages from official or user-configured sources when requested. Those packages remain governed by their own terms and licenses.

Users are responsible for complying with:

- Minecraft EULA: https://www.minecraft.net/eula
- Minecraft Usage Guidelines: https://www.minecraft.net/usage-guidelines
- Licenses for server software, plugins, mods, Java, Multipass, and Ubuntu

See:

- `EULA.md`
- `APP_STORE_README.md`

## Supported Server Types

- Minecraft Bedrock Edition
- Vanilla Java
- CraftBukkit
- Spigot
- Paper
- Fabric
- Forge
- Sponge/SpongeVanilla

## Bedrock Runtime

Mojang publishes Bedrock Dedicated Server for Linux, not as a native macOS binary. MacMine uses Canonical Multipass to run an Ubuntu VM and starts Mojang's Linux Bedrock server package from the mounted MacMine server folder.

Bedrock setup includes:

- Multipass install/open-installer flow.
- Multipass status checks.
- One MacMine VM per Bedrock server profile.
- VM folder mount.
- UDP forwarding from the selected Mac network address to the Bedrock VM.
- Local connection test.
- LAN discovery toggle.

MacMine waits for Multipass before downloading Mojang's Bedrock Linux package.

## Plugins And Mods

MacMine does not bundle plugin or mod jars.

The Plugins & Mods panel can:

- Show common API capability labels for server types.
- Import a user-selected `.jar`.
- Move `.jar` files between active and disabled folders.
- Open the plugin/mod folder.
- Refresh the folder scan.

Displayed capability labels include Bukkit API, Spigot API, Paper API, Fabric API, Forge mods folder, and Sponge plugins folder.


