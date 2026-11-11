# Changelog

All notable changes to `LeafSleep` are documented in this file.

## [Unreleased]

## [1.0.0] - Unreleased

### Added
- Initial multi-loader release of `LeafSleep` (`Paper`, `Spigot`, `Folia`, `Fabric`, `NeoForge`, `Velocity`).
- Implemented `ShardSleepCoordinator` with `logistic`, `linear`, `step`, and `sqrt` quorum curves (`ONE_PLAYER`, `PERCENTAGE`, `FIXED_COUNT`, and `ABSOLUTE_MAJORITY` legacy aliases), `tug of war` and `threshold` cancel policies, warmup countdown (`warmupActionBar`, `warmupBossBar`), gradual dawn easing (`increment`, `timeBetweenIncrements`), cross-shard `/sleep cancel`, and idempotent `targetDayEpoch` CAS dawn transitions (`leafsleep-ADR-001`).
- Implemented `SleepSyncTransport` (Direct TCP/UDP HMAC-signed peer gossip, `leafsleep:sync` plugin messaging, Redis pub/sub, and local-only modes) guarded by `BudgetPacer`.
- Implemented `SleepDatabaseStore` asynchronous SQL persistence (`SQLite`, `MySQL`, `MariaDB`, `PostgreSQL`) for player sleep preferences and theme selections (`leafsleep_player_prefs`), cooldowns, counters, and shard group epoch watermarks (`leafsleep_shard_group_epochs`).
- Added `/sleep` (`/ops`) command tree (`status`, `sleep [messageId]`, `message [id|random]`, `cancel`, `ignore`, `reload`, `test`), externalized message themes in `messages/*.yml` (`default`, `cozy`, `starlight`, `campfire`, `phantom`, `nightmare`, `rooster`, `lazy`), and `[OPS bit]` PBIT/CBIT/IBIT self-tests (`leafsleep-ADR-002`).
