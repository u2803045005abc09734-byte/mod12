# Waterfall Particles (Fabric, Minecraft 26.3)

A client-side Fabric mod that adds small spray particles beside vertical flowing water.

## Build on GitHub Actions

1. Upload the complete contents of this folder to the root of your GitHub repository.
2. Confirm that these two Java files stay at their separate paths:
   - `src/client/java/dev/phoenix/waterfallparticles/client/WaterfallParticlesClient.java`
   - `src/client/java/dev/phoenix/waterfallparticles/client/particle/CascadeParticle.java`
3. Commit and push. The workflow at `.github/workflows/build.yml` will build the mod.
4. Download `WaterfallParticles-Fabric-26.3` from the successful GitHub Actions run.

## Important: avoid the duplicate-class error

`WaterfallParticlesClient.java` must contain `public final class WaterfallParticlesClient`, not `public final class CascadeParticle`.
The `CascadeParticle` class belongs only in `src/client/java/dev/phoenix/waterfallparticles/client/particle/CascadeParticle.java`.
Do not paste the `CascadeParticle.java` source over `WaterfallParticlesClient.java`.

This mod is client-side (`environment: client`). Each player who wants to see the effect must install it in their client `mods` folder.
