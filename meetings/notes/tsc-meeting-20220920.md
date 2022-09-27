# TSC Meeting 2022-09-13 Notes

## Attendees

- Karl Berg
- Nicholas Lawson
- Royal O'Brien
- Jeremy Ong
- Tobias Franke

## Agenda

### [Mobile SIG](https://github.com/o3de/tsc/issues/51#issuecomment-1252477332)

- Discussion is still active here: https://github.com/o3de/tsc/discussions/46
- Will be raised at next joint SIG/TSC meeting to solicit broader feedback

### [Parallel Test issue discussion](https://github.com/o3de/o3de/issues/9295)

- Not strictly a TSC issue, concerns tests that break under simultaneous execution stochastically
- Recommendation is that SIG test reassign problematic test back to SIG that authored the test
- Suggested that there be a simple option to disable concurrent test execution in rare cases where it is needed (e.g. editor framework tests)
- Expectation is that for the most parts, tests that only pass when run in isolation are, in fact, faulty tests

### Question regarding new website/blog workflow

- Concern raised from sig-docs/community that the new blog CMS and process doesn't allow the same feedback mechanisms offered by GitHub
- Ultimately not directly a TSC concern, but suggested that a conversation start first directly between the docs SIG and the marketing committee
- Suggested that Github could be used as an ingestion mechanism to the CMS process proposed by marketing but that the suggested process would need to be put in writing
