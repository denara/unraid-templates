# denara's unofficial Unraid integrations

Unraid® is a registered trademark of Lime Technology, Inc. This application is not affiliated with, endorsed, or sponsored by Lime Technology, Inc.

Public Community Applications templates. The application source and container pipeline live in
[denara/solidcraft-unraid](https://github.com/denara/solidcraft-unraid/tree/codex/unraid-mcp-web).

## SolidCraft — unofficial Unraid integration

The CAD engine and browser application are developed by bherbruck and the upstream SolidCraft contributors.
denara maintains only the container packaging, HTTP MCP adapter and Unraid template.

Experimental Linux amd64 packaging of the independent SolidCraft browser CAD application and
an authenticated Streamable HTTP MCP service. The web app and MCP use separate CAD models.
Upstream: [bherbruck/solidcraft](https://github.com/bherbruck/solidcraft).

Image: `ghcr.io/denara/solidcraft-unraid:latest`. The moving tag is published only after the
container passes modelling, separate-session, file/authentication/origin, restart and web checks.
Commit-specific `sha-<full-source-commit>` tags identify earlier builds for controlled rollback.
No CAD kernel development or upstream application release is implied by these container builds.

The CA portal received and automatically approved the repository on 2026-10-12 as
**denara's Repository**. It says the Docker app should appear after the next CA build publishes.
Install **SolidCraft** through Unraid Community Applications once the listing is visible.
Until the listing appears, download
`templates/solidcraft.xml` and use it as a user template, or place it under
`/boot/config/plugins/community.applications/private/denara/` for local CA use.
The template requires an appdata mapping and a deployment-specific allowed HTTPS origin.
No hostname, server address, token or user design is included here.

Configuration and deployment: [Unraid guide](https://github.com/denara/solidcraft-unraid/blob/codex/unraid-mcp-web/docs/unraid.md).
Support: [packaging issues](https://github.com/denara/solidcraft-unraid/issues).

Back up designs before updates. Keep the same `/data` mapping and MCP token. Browser designs
are stored separately in the browser and need their own export/backup. `latest` is experimental,
not a guarantee that every CAD operation is supported. This is not an official upstream package.

## License and attribution

Templates and documentation are provided under the MIT license in `LICENSE`.
`icons/solidcraft.png` is generated from the original SolidCraft CLI icon renderer
(`solvecraft-cli icon --size 256`), by SolidCraft contributors, licensed MIT OR Apache-2.0.
Source: [CLI renderer](https://github.com/denara/solidcraft-unraid/blob/codex/unraid-mcp-web/apps/solvecraft-cli/src/main.rs).