> `Changelog:`
> - All significant changes to this project will be documented here.
---

> [5.0.0]
>
> - Migrated shell from `bash` to `sh` for broader compatibility and faster execution.
> - Introduced a lockfile system to prevent duplicate execution.
> - Added SQLite optimization with size filtering (skip files >100MB).
> - Implemented I/O tuning (scheduler, read-ahead, noatime, zRAM setup).
> - Added memory tuning based on total RAM (drop caches, swappiness, lowmemorykiller tuning).
> - Integrated UI optimization through SurfaceFlinger system properties.
> - Added gaming mode optimizations (CPU/GPU frequency scaling, kernel scheduler tuning).
> - Included ART optimization for application performance (cmd package compile).
> - Performed automatic fstrim on core partitions to reduce write amplification.
> - Removed logging and remount logic for lighter and safer runtime optimization.
> - Dropped legacy `.rc` file optimization and background logging to focus on runtime performance.
> - And there are many other small changes.
---

> [4.0.0]
>
> - Added new modules or functions to improve the performance and functionality of the system.
> - Updated the documentation with the latest information on using new features.
> - Reorganized directories and files to make code maintenance easier.
> - Refactored code to improve performance and stability.
> - Fixed a bug in a module that previously caused an error when inserting data.
> - Improved validation and error checking to prevent potential security holes.
> - Removed functions or code that are no longer relevant and unused.
> - Cleaned up unnecessary code to optimize system performance.
---

> [3.5.0]
>
> - Version Update.
---

> [1.0.0]
>
> - Initial release.
---
