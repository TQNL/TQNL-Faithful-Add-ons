# Compatibility and test scope

The 32x and 64x item add-ons cover **Minecraft 1.17–26.3** through one ZIP per resolution. This covers all 34 stable releases in that interval. Later items are included only where the client contains them; the pack does not create items or enable experiments.

The root contains the original sixteen waxed copper items in the legacy item-model layout. Overlays add later copper items, select the 1.21.4 item definitions and retain the accepted 1.21.9+ statue rendering, including the 26.1 transformation.

## Older clients

The single legacy `pack_format` marker is 15. **Minecraft 1.17–1.19.4 shows a “too new” warning and requires manual enabling.** Those clients can load the supplied legacy item assets, but they ignore the newer compatibility range. Minecraft 1.20/1.20.1 matches the single marker; later clients read the declared range and overlays.

See [Mojang's 1.20.2 format notes](https://www.minecraft.net/en-us/article/minecraft-java-edition-1-20-2) and [the later combined-format declarations](https://www.minecraft.net/en-us/article/minecraft-snapshot-25w31a). The exact client loaders were used to verify these declarations; the warning is not reported as a green compatibility classification.

## Faithful sources

The earlier 32x copper source artwork matches the pinned modern originals. The 64x pack uses historical original Faithful copper families where they differ, with the same precise wax masks. No exact official 64x 1.17/1.18 export was found on the audited distribution channels, so those versions use a native-UV backport of original Faithful 1.19 copper art.

Some exact exports are absent and some client patches share a resource format. Those clients receive the matching neighboring original family; 1.20.3 and 1.20.4 share format 22 and both use the newer 1.20.4 artwork. Experimental copper items absent from an older Faithful export use the pinned later original artwork. Each ZIP includes source provenance, credits and applicable license notices.

## Verification

- **68 exact native loader checks:** both editions through all 34 official clients, including metadata parsing, native overlay selection and complete resolved resource hashes. Modern clients classify the pack as compatible; the earlier clients report the warning above.
- **68 independent reference checks:** native item availability, recursive model parents, face texture aliases, generated layers and item definitions against each exact official client.
- Pre-1.21.9 checks also use the native model deserializers and available native item-definition codecs. Modern resources remain byte-identical to the reviewed V3 artwork and rendering resources.
- The retained Minecraft **26.3** visual review covers 72 inventory renders and 12 rotated lightning rods per edition. No new historical in-game visual matrix is claimed.

[Native and reference test record](compatibility-tests.json) · [Deterministic build and resource-map record](compatibility-build.json).

The source builder, pinned original artwork and full compatibility notes are in the [Faithful Vanilla Tweaks repository](https://github.com/TQNL/TQNL-Faithful-Vanilla-Tweaks/blob/main/visual-copper/docs/legacy-copper-compatibility.md). Placed blocks and live golems are unchanged. The full tweaks compilation retains its own 1.21+ interval, and the separate 16x statue patch starts at 1.21.9.
