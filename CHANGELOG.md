# Changes in Jupyter Client {#changelog}

<!-- <START NEW CHANGELOG ENTRY> -->

## 7.0.0rc1

([Full Changelog](https://github.com/jupyter/jupyter_client/compare/7.0.0rc0...dcfd103f707a67627850b190a2323dd621ed46ae))

### Maintenance and upkeep improvements

- Prepare for use with Jupyter Releaser [#676](https://github.com/jupyter/jupyter_client/pull/676) ([@afshin](https://github.com/afshin))
- Fix project name [#674](https://github.com/jupyter/jupyter_client/pull/674) ([@vidartf](https://github.com/vidartf))

### Contributors to this release

([GitHub contributors page for this release](https://github.com/jupyter/jupyter_client/graphs/contributors?from=2021-08-05&to=2021-08-11&type=c))

[@afshin](https://github.com/search?q=repo%3Ajupyter%2Fjupyter_client+involves%3Aafshin+updated%3A2021-08-05..2021-08-11&type=Issues) | [@vidartf](https://github.com/search?q=repo%3Ajupyter%2Fjupyter_client+involves%3Avidartf+updated%3A2021-08-05..2021-08-11&type=Issues)

<!-- <END NEW CHANGELOG ENTRY> -->

## 7.0.0rc0

### Enhancements made

- Kernel Provisioning - initial implementation
  [#612](https://github.com/jupyter/jupyter_client/pull/612)
- Added debugger key in `kernel_info_reply` [#486](https://github.com/jupyter/jupyter_client/pull/486)

### Bugs fixed

- Fix up some async method aliases in `KernelManager`
  [#670](https://github.com/jupyter/jupyter_client/pull/670)
- Support `nswer_yes` when removing kernel specs
  [#659](https://github.com/jupyter/jupyter_client/pull/659)
- Include process ID in message ID [#655](https://github.com/jupyter/jupyter_client/pull/655)

### Maintenance and upkeep improvements

- Rename trait to `allowed_kernelspecs` [#672](https://github.com/jupyter/jupyter_client/pull/672)
- Remove block parameter from `get_msg()` [#671](https://github.com/jupyter/jupyter_client/pull/671)
- Only import `nest_asyncio` locally [#665](https://github.com/jupyter/jupyter_client/pull/665)
- Use a default serializer that is not only for date types
  [#664](https://github.com/jupyter/jupyter_client/pull/664)
- Updated `debug_info_response` [#657](https://github.com/jupyter/jupyter_client/pull/657)
- Don't block on exit [#651](https://github.com/jupyter/jupyter_client/pull/651)
- Update test kernel with native coroutine, remove `async_generator`
  dependency [#646](https://github.com/jupyter/jupyter_client/pull/646)
- `setup.py` and CI improvements [#645](https://github.com/jupyter/jupyter_client/pull/645)
- Test downstream projects [#644](https://github.com/jupyter/jupyter_client/pull/644)
- Remove deprecations in kernel manager [#643](https://github.com/jupyter/jupyter_client/pull/643)
- Add `block=True` back to `get_msg()` [#641](https://github.com/jupyter/jupyter_client/pull/641)

### Documentation improvements

- Added documentation for `richInspectVariables` request
  [#654](https://github.com/jupyter/jupyter_client/pull/654)
- Change to `edit_magic` payload [#652](https://github.com/jupyter/jupyter_client/pull/652)
- Added missing documentation for the `inspectVariables` request and
  response [#649](https://github.com/jupyter/jupyter_client/pull/649)
- Add status field to other replies in documentation
  [#648](https://github.com/jupyter/jupyter_client/pull/648)

## 6.2.0

- Yanked (PyPI) and marked as broken (conda)

## 6.1.13

- Yanked (PyPI) and marked as broken (conda)

## 6.1.12

- Shutdown request sequence has been modified to be more graceful, it
  now is preceded by interrupt, and will also send a `SIGTERM` before
  forcibly killing the kernel. [#620](https://github.com/jupyter/jupyter_client/pull/620)
- Removal of `ipython_genutils` as a dependency. It was implicit
  before; but required by at least traitlets thus avoiding issues. We
  are working on completely removing it from all jupyter dependencies;
  as it might lead to issues packaging for Python 3.10, and was mostly
  used for compatibility with python 2. ([#620](https://github.com/jupyter/jupyter_client/pull/620), [#605](https://github.com/jupyter/jupyter_client/pull/605))
- Address a race condition between `shutdown_kernel` and restarter.
  ([#607](https://github.com/jupyter/jupyter_client/pull/607).)

See the [full list of
pull-requests](https://github.com/jupyter/jupyter_client/milestone/27?closed=1)

## 6.1.11

- Move jedi pinning to test requirements [#599](https://github.com/jupyter/jupyter_client/pull/599)

## 6.1.10

- Add change parameter needed for observer method of
  kernel_spec_manager trait [#598](https://github.com/jupyter/jupyter_client/pull/598)

## 6.1.9

- Pin jedi\<=0.17.2 [#596](https://github.com/jupyter/jupyter_client/pull/596)

## 6.1.8

- Doc updates ([#563](https://github.com/jupyter/jupyter_client/pull/563),
  [#564](https://github.com/jupyter/jupyter_client/pull/564), [#587](https://github.com/jupyter/jupyter_client/pull/587))
- Fix path to the connection file [#568](https://github.com/jupyter/jupyter_client/pull/568)
- Code cleanup ([#574](https://github.com/jupyter/jupyter_client/pull/574),
  [#579](https://github.com/jupyter/jupyter_client/pull/579))
- Silence kill_kernel when no process is present
  [#576](https://github.com/jupyter/jupyter_client/pull/576)
- Remove extra_env and corresponding test [#581](https://github.com/jupyter/jupyter_client/pull/581)
- Add documentation dependencies to setup.py [#582](https://github.com/jupyter/jupyter_client/pull/582)
- Fix for Windows localhost IP addresses [#584](https://github.com/jupyter/jupyter_client/pull/584)
- Drop Travis CI, add GitHub Actions [#586](https://github.com/jupyter/jupyter_client/pull/586)
- Adapt KernelManager.\_kernel_spec_manager_changed to observe
  [#588](https://github.com/jupyter/jupyter_client/pull/588)
- Allow use \~/ in the kernel\'s command or its arguments
  [#589](https://github.com/jupyter/jupyter_client/pull/589)
- Change wait_for_ready logic [#592](https://github.com/jupyter/jupyter_client/pull/592)
- Fix test_session with msgpack v1 [#594](https://github.com/jupyter/jupyter_client/pull/594)

## 6.1.6

- Removed warnings in more cases for KernelManagers that use new
  cleanup method [#560](https://github.com/jupyter/jupyter_client/pull/560)
- Some improved tests with a conversion to pytest pattern
  [#561](https://github.com/jupyter/jupyter_client/pull/561)

## 6.1.5

- Gracefully Close ZMQ Context upon kernel shutdown to fix memory leak
  [#548](https://github.com/jupyter/jupyter_client/pull/548)
- Fix for chained exceptions to preserve stacks
  ([#552](https://github.com/jupyter/jupyter_client/pull/552), [#554](https://github.com/jupyter/jupyter_client/pull/554))
- Fix start_kernel error when passing kernel_id
  [#547](https://github.com/jupyter/jupyter_client/pull/547)
- Update to releasing docs [#543](https://github.com/jupyter/jupyter_client/pull/543)

## 6.1.4

(Deleted release with incorrect local files)

## 6.1.3

- Add AsyncKernelClient client_class to AsyncKernelManager
  [#542](https://github.com/jupyter/jupyter_client/pull/542)
- Doc fix for xeus hyperlinks [#540](https://github.com/jupyter/jupyter_client/pull/540)
- Doc typo fix [#539](https://github.com/jupyter/jupyter_client/pull/539)

## 6.1.2

- Fixed a bug causing clients to sometimes hang after a stop call was
  made [#536](https://github.com/jupyter/jupyter_client/pull/536)

## 6.1.1

- Subprocess kill action fix for async execution
  [#535](https://github.com/jupyter/jupyter_client/pull/535)
- Doc fix for xeus kernel list [#534](https://github.com/jupyter/jupyter_client/pull/534)

## 6.1.0

This release includes support for asyncio patterns! Downstream tools
should soon have releases to additionally support async patterns.

- AsyncKernelManager and AsyncMultiKernelManager are now available for
  async jupyter_client interactions ([#528](https://github.com/jupyter/jupyter_client/pull/528), [#529](https://github.com/jupyter/jupyter_client/pull/529))
- Removed unused sphinx dependency ([#518](https://github.com/jupyter/jupyter_client/pull/518), [#518](https://github.com/jupyter/jupyter_client/pull/518)).
- Added install instructions for pip to documentation
  [#521](https://github.com/jupyter/jupyter_client/pull/521)
- Improved docs around version protocol and messaging
  ([#522](https://github.com/jupyter/jupyter_client/pull/522), [#526](https://github.com/jupyter/jupyter_client/pull/526))

## 6.0.0

The git history had to be reworked heavily in merging 5.x and master, so
a link to all the changes at once in github had been left out as it\'s
just confusing.

An exciting change in this release is some async support (huge thanks to
\@davidbrochart for doing most of the work)! See linked PR below for
more details, we\'re working on integrating this into nbclient as well
in the near future.

New Features:

- Added async API [#506](https://github.com/jupyter/jupyter_client/pull/506)

Changes:

- Python 3.8 testing and support added [#509](https://github.com/jupyter/jupyter_client/pull/509)
- Session.msg_id optimization [#493](https://github.com/jupyter/jupyter_client/pull/493)
- Only cache ports if the cache_ports flag is set to True
  [#492](https://github.com/jupyter/jupyter_client/pull/492)
- Removed direct dependency on pywin32 as this is now in jupyter core
  [#489](https://github.com/jupyter/jupyter_client/pull/489)

Fixes:

- Prevent two kernels to have the same ports [#490](https://github.com/jupyter/jupyter_client/pull/490)

Docs:

- Document the handling of error in do_execute
  [#500](https://github.com/jupyter/jupyter_client/pull/500)

Breaking changes:

- Dropped support for Python 2.7!

## 5.3.5

- Backported memory leak fix [#548](https://github.com/jupyter/jupyter_client/pull/548)
  [#555](https://github.com/jupyter/jupyter_client/pull/555).

## 5.3.4

- Changed secure_write to be imported from jupyter_core with fix for
  extended usernames in Windows [#483](https://github.com/jupyter/jupyter_client/pull/483).

## 5.3.3

- Fixed issue with non-english windows permissions
  [#478](https://github.com/jupyter/jupyter_client/pull/478). Potential issue still open
  in use with jupyerlab.

## 5.3.2

- Important files creation now checks umask permissions
  [#469](https://github.com/jupyter/jupyter_client/pull/469).

## 5.3.1

- Fix bug with control channel socket introduced in 5.3.0
  [#456](https://github.com/jupyter/jupyter_client/pull/456).

## 5.3.0

[5.3.0 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/5.3.0)

New Features:

- Multiprocessing and Threading support [#437](https://github.com/jupyter/jupyter_client/pull/437) and [#450](https://github.com/jupyter/jupyter_client/pull/450)
- Setup package long_description [#411](https://github.com/jupyter/jupyter_client/pull/411)

Changes:

- Control channel now in the public API [#447](https://github.com/jupyter/jupyter_client/pull/447)
- Closing Jupyter Client is now faster [#420](https://github.com/jupyter/jupyter_client/pull/420)
- Pip support improvements [#421](https://github.com/jupyter/jupyter_client/pull/421)

Breaking changes:

- Dropped support for Python 3.3 and 3.4 (upstream packages dropped
  support already)

## 5.2.4

[5.2.4 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/5.2.4)

- Prevent creating new console windows on Windows
  [#346](https://github.com/jupyter/jupyter_client/pull/346)
- Fix interrupts on Python 3.7 on Windows [#408](https://github.com/jupyter/jupyter_client/pull/408)

## 5.2.3

[5.2.3 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/5.2.3)

- Fix hang on close in `.ThreadedKernelClient` (used in QtConsole) when using tornado with asyncio
  (default behavior of tornado 5, see [#352](https://github.com/jupyter/jupyter_client/pull/352)).
- Fix errors when using deprecated
  `.KernelManager.kernel_cmd`
  ([#343](https://github.com/jupyter/jupyter_client/pull/343), [#344](https://github.com/jupyter/jupyter_client/pull/344)).

## 5.2.2

[5.2.2 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/5.2.2)

- Fix `.KernelSpecManager.get_all_specs` method in subclasses that only override
  `.KernelSpecManager.find_kernel_specs` and
  `.KernelSpecManager.get_kernel_spec`.
  See [#338](https://github.com/jupyter/jupyter_client/issues/338) and
  [#339](https://github.com/jupyter/jupyter_client/pull/339).
- Eliminate occasional error messages during process exit
  [#336](https://github.com/jupyter/jupyter_client/pull/336).
- Improve error message when attempting to bind on invalid address
  [#330](https://github.com/jupyter/jupyter_client/pull/330).
- Add missing direct dependency on tornado [#323](https://github.com/jupyter/jupyter_client/pull/323).

## 5.2.1

[5.2.1 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/5.2.1)

- Add parenthesis to conditional pytest requirement to work around a
  bug in the `wheel` package, that generate a `.whl` which otherwise
  always depends on `pytest` see [#324](https://github.com/jupyter/jupyter_client/issues/324)and [#325](https://github.com/jupyter/jupyter_client/pull/325).

## 5.2

[5.2 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/5.2)

- Define Jupyter protocol version 5.3:
  - Kernels can now opt to be interrupted by a message sent on the
    control channel instead of a system signal. See
    `kernelspecs` and
    `msging_interrupt`
    [#294](https://github.com/jupyter/jupyter_client/pull/294).
- New `jupyter kernel` command to launch an installed kernel by name
  [#240](https://github.com/jupyter/jupyter_client/pull/240).
- Kernelspecs where the command starts with e.g. `python3` or
  `python3.6`---matching the version `jupyter_client` is running
  on---are now launched with the same Python executable as the
  launching process [#306](https://github.com/jupyter/jupyter_client/pull/306). This
  extends the special handling of `python` added in 5.0.
- Command line arguments specified by a kernelspec can now include
  `{resource_dir}`, which will be substituted with the kernelspec
  resource directory path when the kernel is launched
  [#289](https://github.com/jupyter/jupyter_client/pull/289).
- Kernelspecs now have an optional `metadata` field to hold arbitrary
  metadata about kernels---see `kernelspecs` [#274](https://github.com/jupyter/jupyter_client/pull/274).
- Make the `KernelRestarter` class used by a `KernelManager`
  configurable [#290](https://github.com/jupyter/jupyter_client/pull/290).
- When killing a kernel on Unix, kill its process group
  [#314](https://github.com/jupyter/jupyter_client/pull/314).
- If a kernel dies soon after starting, reassign random ports before
  restarting it, in case one of the previously chosen ports has been
  bound by another process [#279](https://github.com/jupyter/jupyter_client/pull/279).
- Avoid unnecessary filesystem operations when finding a kernelspec
  with `.KernelSpecManager.get_kernel_spec` [#311](https://github.com/jupyter/jupyter_client/pull/311).
- `.KernelSpecManager.get_all_specs`
  will no longer raise an exception on encountering an invalid
  `kernel.json` file. It will raise a warning and continue
  [#310](https://github.com/jupyter/jupyter_client/pull/310).
- Check for non-contiguous buffers before trying to send them through
  ZMQ [#258](https://github.com/jupyter/jupyter_client/pull/258).
- Compatibility with upcoming Tornado version 5.0
  [#304](https://github.com/jupyter/jupyter_client/pull/304).
- Simplify setup code by always using setuptools
  [#284](https://github.com/jupyter/jupyter_client/pull/284).
- Soften warnings when setting the sticky bit on runtime files fails
  [#286](https://github.com/jupyter/jupyter_client/pull/286).
- Various corrections and improvements to documentation.

## 5.1

[5.1 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/5.1)

- Define Jupyter protocol version 5.2, resolving ambiguity of
  `cursor_pos` field in the presence of unicode surrogate pairs.

  ::: {.seealso}
  `cursor_pos_unicode_note`
  :::

- Add `Session.clone` for making a copy
  of a Session object without sharing the digest history. Reusing a
  single Session object to connect multiple sockets to the same IOPub
  peer can cause digest collisions.

- Avoid global references preventing garbage collection of background
  threads.

## 5.0

#### 5.0.1

[5.0.1 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/5.0.1)

- Update internal protocol version number to 5.1, which should have
  been done in 5.0.0.

#### 5.0.0

[5.0.0 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/5.0)

New features:

- Implement Jupyter protocol version 5.1.

- Introduce `jupyter run` command
  for running scripts with a kernel, for instance:

      jupyter run --kernel python3 myscript.py

- New method
  `.BlockingKernelClient.execute_interactive` for running code and capturing or redisplaying its
  output.

- New `KernelManager.shutdown_wait_time` configurable for adjusting
  the time for a kernel manager to wait after politely requesting
  shutdown before it resorts to forceful termination.

Fixes:

- Set sticky bit on connection-file directory to avoid getting cleaned
  up.
- `jupyter_client.launcher.launch_kernel` passes through additional options to the underlying
  Popen, matching `KernelManager.start_kernel`.
- Check types of `buffers` argument in
  `.Session.send`, so that TypeErrors
  are raised immediately, rather than in the eventloop.

Changes:

- In kernelspecs, if the executable is the string `python` (as opposed
  to an absolute path), `sys.executable` will be used rather than
  resolving `python` on PATH. This should enable Python-based kernels
  to install kernelspecs as part of wheels.
- kernelspec names are now validated. They should only include ascii
  letters and numbers, plus period, hyphen, and underscore.

Backward-incompatible changes:

- :py`.datetime` objects returned in
  parsed messages are now always timezone-aware. Timestamps in
  messages without timezone info are interpreted as the local
  timezone, as this was the behavior in earlier versions.

## 4.4

#### 4.4.0

[4.4 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/4.4)

- Add `.KernelClient.load_connection_info` on KernelClient, etc. for loading connection info
  directly from a dict, not just from files.
- Include parent headers when adapting messages from older protocol
  implementations (treats parent headers the same as headers).
- Compatibility fixes in tests for recent changes in ipykernel.

## 4.3

#### 4.3.0

[4.3 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/4.3)

- Adds `--sys-prefix` argument to
  `jupyter kernelspec install`, for
  better symmetry with `jupyter nbextension install`, etc.

## 4.2

#### 4.2.2

[4.2.2 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/4.2.2)

- Another fix for the `start_new_kernel` issue in 4.2.1 affecting slow-starting kernels.

#### 4.2.1

[4.2.1 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/4.2.1)

- Fix regression in 4.2 causing `start_new_kernel` to fail while waiting for kernels to become available.

#### 4.2.0

[4.2.0 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/4.2)

- added `jupyter kernelspec remove`
  for removing kernelspecs
- allow specifying the environment for kernel processes via the `env`
  argument
- added `name` field to connection files identifying the kernelspec
  name, so that consumers of connection files (alternate frontends)
  can identify the kernelspec in use
- added `KernelSpecManager.get_all_specs` for getting all kernelspecs more efficiently
- various improvements to error messages and documentation

## 4.1

#### 4.1.0

[4.1.0 on
GitHub](https://github.com/jupyter/jupyter_client/milestones/4.1)

Highlights:

- Setuptools fixes for `jupyter kernelspec`
- `jupyter kernelspec list` includes paths
- add `KernelManager.blocking_client`
- provisional implementation of `comm_info` requests from upcoming 5.1
  release of the protocol

## 4.0

The first release of Jupyter Client as its own package.
