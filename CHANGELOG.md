> `Changelog:`
> - All significant changes to this project will be documented here.
---

> [7.0.0] `Final`
>
> - Update or change `README.md` to make it more professional.
> - Update `README.md` to be a little more professional.
> - Update the `customize.sh` section with a few changes.
> - Slightly improved `arch` detection in customize.sh for device extensions.
> - Updated `uninstall.sh` with minor changes to the removal code.
> - Add module banner for KernelSU Next.
> - Tidying up and making a few code changes in the `service.sh` file.
> - Moved `optimize_sqlite` optimization to service.sh for better optimization.
> - Added notification every time tweaks are successfully completed.
> - Introduced thermal control module (`disable_thermal`) to disable throttling, services, and thermal limits aggressively.
> - Added GPU optimization module (`gpu_optimize`) with extended support for governors, max/min frequency tuning, bus governor, and throttling control.
> - Implemented Touch optimization module (`touch_optimize`) for sensitivity, boost level, polling, and input boost frequency tuning.
> - Added Entropy optimization module (`entropy_optimize`) with rng selection, jitterentropy support, and stricter kernel entropy settings.
> - Introduced Kernel optimization module (`kernel_optimize`) to disable unnecessary logging, panic, and enhance OOM handling.
> - Reworked I/O optimization logic (`tune_io`) with adaptive scheduler selection based on RAM profile, improved affinity, readahead, and mount options.
> - Improved ZRAM setup (`setup_zram`) with dual device support, adaptive compression algorithm, and balanced sizing based on total RAM.
> - Enhanced Memory optimization (`tune_memory`) with new sysctl parameters, adaptive profiles (Gaming, Balanced, Performance), and better lowmemorykiller settings.
> - Expanded UI optimization (`ui_optimize`) with more SurfaceFlinger, HWUI, EGL, and rendering properties for smoother performance.
> - Improved Game optimization (`game_opt`) with stricter CPU/GPU tuning, kernel scheduler tweaks, and notification disabling for gaming focus.
> - Added sequential execution delays between modules (`sleep 5`) for stability and controlled runtime execution.
> - General refactoring and code cleanup for stability, modularity, and maintainability.
---

> [6.0.0]
>
> - Minor code fixes in `uninstall.sh` to make it more optimal.
> - Moved the `optimize_art` section into service.sh now, to make the process a bit faster than before.
> - Check and fallback for availability of `sqlite3`, `setprop`, and other commands.
> - Avoid forcing chmod 660 if the permissions are already correct in `optimize_sqlite`.
> - Separated ZRAM logic from `tune_io` and moved it into its own function `setup_zram` for better modularity.
> - Improved memory optimization with additional sysctl parameters such as `page-cluster`, `dirty_writeback_centisecs`, and KSM control.
> - Added fail-safe write checks (`[ -w ... ]`) before applying sysctl values to prevent unnecessary errors.
> - Enhanced game performance tuning with scheduler tweaks like `sched_child_runs_first` and `sched_idle_min_granularity_ns`.
> - Expanded GPU max frequency detection to support more device paths.
> - Removed direct call to `optimize_art` in `main`, as it's now managed separately by `service.sh`.
> - General code cleanup for safety, modularity, and efficiency.
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