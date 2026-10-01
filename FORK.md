# This fork

`peakpassvpn/route_manager` is a fork of [tun-rs/route_manager](https://github.com/tun-rs/route_manager), used by [sail](https://github.com/peakpassvpn/sail) through `[patch.crates-io]`.

- **Branch:** `sail`, which is upstream `main` plus the commits below. Upstream is merged into it, never rebased: sail pins revisions of this branch.
- **Why:** upstream depends on netlink-packet-core 0.8, which pulls in `paste` (unmaintained, RUSTSEC-2024-0436). This branch moves to netlink-packet-core 0.9 and netlink-packet-route 0.33; the code is unchanged.
- **Drop it when:** upstream releases a version on netlink-packet-core 0.9 or later. sail then removes its patch and this fork is archived.
- **Checked by:** sail's weekly upstream report (`tools/upstream-watch`).
