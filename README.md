# AOSPlop

AOSPlop plops the LaydibugOS AOSP source tree onto your disk.

```
./AOSPlop
```

That's it. No flags. If it works, you get a materialized Android source tree.
If it doesn't, sorry bro.

## Status

**V1.** Currently plops exactly ONE file (`external/ffmpeg/LICENSE.md`).

The rest of the tree is coming. Each OUTTIE in our source tree needs its
upstream chain closed on our end before we add it here. See the
clean-license-audit arc.

## Scope

AOSPlop is a public, python-diaper, single-shot script that reconstructs
the LaydibugOS AOSP source tree from public upstream sources plus a small
bundled payload of files we authored ourselves. Think of it as a
convoluted but completely transparent fae-program at the whole-tree scale.

It is **intentionally** low-effort. You run one command. It materializes
the tree or it does nothing. There are no flags, no modes, no settings,
no SBOM, no verification mode. If you want proper version control for
Android development, you want a different tool (hint: jellibeen, coming).

## Requirements

Python 3. Internet. A disk.

Worked on my machine (Ubuntu 24.04, 2026-10-28). If it doesn't work on
yours, PRs welcome but we won't maintain compatibility.

## Why it's shaped like this

- **Legal transparency.** Reconstructing the tree from first-principles
  public sources is the honest version of "we release source code."
- **Community goodwill.** We actually release the whole tree, not just
  the kernel.
- **Distribution economics.** Shipping a sub-GB script is cheaper than
  hosting an 80GB tree.
- **Accessibility.** Any hobbyist can grab the tree and start building
  Android with their AI assistant of choice.

## License

The AOSPlop script itself: Apache-2.0.
Each file fetched carries its own upstream license.
