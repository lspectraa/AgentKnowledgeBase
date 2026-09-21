# Run, test, lint

Record the real commands for this repo after the first index. Do not invent scripts.

## Concurrent execution

Independent commands may run in the same turn as each other and as reads, searches, edits, or sub-agents, as long as they do not write the same file or share a mutating cwd.

Stay serial when the next command needs the previous result (install before test, build before run).
