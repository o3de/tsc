# TSC Meeting 2022-09-13 Notes

## Attendees

- Karl Berg
- Nick Lawson
- Roddie Kieley
- Jeremy Ong
- Tobias Alexander Franke

## Agenda

### User-License Elections

Quick mention that the Quest 2 SDK will also need a user-provided acceptance of the Quest 2 SDK license.

### Python Dependency discussion

- Q: Are there any considerations the TSC should think of w.r.t. approval of additional Python dependencies fetched via pip?
- One option is to add a logical review group marked as a `CODEOWNER` of the requirements files to make the dependency changes more visible in a PR
- No additional security considerations were thought of, although 3rd party libs that are vendored via O3DF have a smaller vulnerability surface area
- For C++ deps, it was mentioned that CMake's `FetchProject` functions may be more suitable, but SIG-Build may need to provide a convenient cmake macro to disable/enable compiler warnings
- For now, continue to rely on SIGs to vet dependencies added via Python or any other means

### o3de-extras

- PSA that SIGs should include issues and PRs filed against the o3de-extras repo as part of their triage process.
- Suggestion was made to make o3de-extras more discoverable via the TL README in the primary o3de repo
- Q: What determines what goes in o3de vs o3de-extras (A: SIGs should generally decide for their respective domains what gems should be part of the "core" experience vs the extended experience in the interest of keeping the core engine lean but usable)
- Will mention o3de-extra in a subsequent joint meeting
- Migrating existing gems from o3de to o3de-extra will be an ongoing effort
