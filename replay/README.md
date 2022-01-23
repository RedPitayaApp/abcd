# System simulation by replaying data files

**Events files** and **raw files** may be used to simulate a running system.
Raw files contain all the information generated by a running system (_i.e._ status messages, start and stop timestamps, configuration files...).
Using `replay_raw` or `replay_raw.py` a raw file may be replayed simulating a full working system.
`replay_raw.py` also supports raw files compressed with `gzip`, `bzip2`, or `xz`.
If python is not available, the C version of `replay_raw` may be used, but it does not support compressed raw files.

Only `replay_raw.py` supports the replay of `waan` status messages saved in the raw files.
**Warning:** a running istance of `waan` conflicts with `replay_raw.py` if the replay of the `waan` status messages is enabled.

Events files contain only the processed events and can only simulate a stream of processed data.
`replay_events` supports only `.ade` files.