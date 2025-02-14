# Changelog

All notable changes to this project will be documented in this file.

## [0.13.0] - 2024-03-19

### 🚀 Features

- Add rust-ceramic clay bootstrap nodes (#288)

### 🐛 Bug Fixes

- Pass job labels to designate notification channels (#281)
- Remove loud warn from Recon (#287)

### ⚙️ Miscellaneous Tasks

- Delete subscribe endpoint (#277)
- Only lint single commit or PR title (#279)
- Remove support for old event payload during creation (#272)

## [0.12.0] - 2024-02-22

### 🚀 Features

- Create GET endpoint to return events for an interest range (#276)

### 🐛 Bug Fixes

- Use PAT for create-release-pr workflow (#275)
- Honor PENDING_RANGES_LIMIT for initial ranges (#271)

### ⚙️ Miscellaneous Tasks

- Version v0.12.0 (#278)

## [0.11.0] - 2024-02-12

### 🚀 Features

- Enable recon by default (#270)
- Support new id/data event payload for event creation (POST /events) (#269)

### 🐛 Bug Fixes

- Store metrics under own registry (not recon) (#266)

### ⚙️ Miscellaneous Tasks

- Version v0.11.0 (#274)

## [0.10.1] - 2024-02-08

### 🐛 Bug Fixes

- Allow double insert of key/value pairs in Recon (#264)
- Use try_from on recon keys (#263)
- Resume token should return previous (not 0) when nothing found (#265)

### ⚙️ Miscellaneous Tasks

- Version v0.10.1 (#267)

## [0.10.0] - 2024-02-06

### 🚀 Features

- Continously publish provider records (#175)
- Add publisher batch metrics (#187)
- Add config for republish_max_concurrent (#192)
- Add peering support (#194)
- Add tokio metrics (#206)
- Merge migration script with ceramic-one (#190)
- Add metrics to api and recon (#208)
- Schedule_k8s_deploy github action (#213)
- Recon-over-http (#168)
- Remove all usage of gossipsub (#209)
- Stop publishing CIDs to DHT on write (#211)
- On tag publish deploy to envs (#220)
- Add sqlite read/write pool split (#218)
- Add recon store metrics (#221)
- Add value support to Recon (#217)
- Post-deployment tests (#242)
- Updated release workflow (#241)
- Modify recon storage tables, trait and sqlite config to improve throughput (#243)
- Synchronize value for synchronized ranges (#238)
- Workflow_dispatch build job (#249)
- Add unified recon block store implementation (#245)
- Interest registration endpoint (#246)
- Added correctness test (#248)
- Support for set type documents (#259)
- Add API to fetch eventData from event String (#258)
- Add feed endpoint to propagate event data to js-ceramic (#255)

### 🐛 Bug Fixes

- Check limits first before other behaviours (#183)
- Panic with divide by zero duration math (#184)
- Fix JSON log format errors (#185)
- Update comment to pass clippy (#189)
- Run publisher in its own task (#188)
- Trickle publisher keys to swarm (#191)
- Use AIMD for publisher batch size (#195)
- Do not use bootstrap list with kademlia (#199)
- Simplify the publisher (#200)
- Always collect metrics (#202)
- Typo (#203)
- Upgrade to libp2p 0.53 (#205)
- Clippy accessing first element with first (#212)
- Update deploy workflows for k8s (#216)
- Rename workflows (#223)
- Add a BUILD tag if it's not a PR merge (#256)
- Refactor recon storage and remove sqlx dependency from recon and core crates (#254)
- Update git config for release pr workflow

### 🚜 Refactor

- Update bitswap logs to use structured logging (#193)

### ⚙️ Miscellaneous Tasks

- Use latest stable openapi-generator-cli (#222)
- Use docker root user (#251)
- Adding ci for cargo machete (#252)
- Run fast post-deployment tests for all envs (#257)
- Fix false positive in checking generated servers (#260)
- Version v0.10.0 (#261)

## [0.9.0] - 2023-11-13

### 🚀 Features

- Add control over autonat (#176)

### 🐛 Bug Fixes

- Rename iroh to ceramic-one in agent (#181)

### ⚙️ Miscellaneous Tasks

- Pass manual flag through in deployment job (#180)
- Release version v0.9.0 (#182)

## [0.8.3] - 2023-11-09

### 🐛 Bug Fixes

- Call correct api method for removing block from pin store (#178)
- Be explicit about release deployments (#177)

### ⚙️ Miscellaneous Tasks

- Release version v0.8.3 (#179)

## [0.8.2] - 2023-11-08

### 🚀 Features

- Add explicit log format CLI option
- Add ceramic_one_info metric
- Add exe_hash to info
- Default swarm port
- Bootstrap peers
- Add kubo rpc api metrics
- Add cli opts for connection limits
- Add ipfs metrics
- Expose basic kademlia config
- Cd (#172)

### 🐛 Bug Fixes

- Use rust-builder latest
- Remove Ceramic peer discovery
- Readd main.rs after move
- Only provide records on the DHT when they are new
- Work around github's dumb syntax for conditionals (#173)

### 🚜 Refactor

- Move iroh-metrics to ceramic-metrics
- Allow uses of deprecated metrics traits

### ⚙️ Miscellaneous Tasks

- Release version v0.8.2 (#174)

## [0.8.1] - 2023-10-26

### ⚙️ Miscellaneous Tasks

- Add CHANGELOG.md
- Release version v0.8.1

## [0.8.0] - 2023-10-25

### 🚀 Features

- Add offline parameter to block/get

### 🐛 Bug Fixes

- Need to install the openapi generator

### ⚙️ Miscellaneous Tasks

- Add new release pr workflow based on container
- Release version v0.8.0

## [0.7.0] - 2023-10-23

### 🚀 Features

- Allow comma-separated bootstrap addresses

### 🐛 Bug Fixes

- Upgrade ssi to fix incompatibilities
- Kubo rpc alignment
- Remove unique violation error check when inserting block
- Add kubo-rpc api error logs
- Optimize sqlx pool options
- Append peer id to all listen addrs
- Change pubsub/ls to return base64url encoded topics
- Add block get timeout
- Improve API instrumentation
- Update external address handling for kad

### ⚙️ Miscellaneous Tasks

- Remove unused deps
- Cargo update
- Update libp2p to 0.52.4
- Release

## [0.6.0] - 2023-09-20

### 🐛 Bug Fixes

- Use multiline for conditional
- Only check for top level changes

### ⚙️ Miscellaneous Tasks

- Release (#130)
- Release (#131)

## [0.4.0] - 2023-09-20

### 🚀 Features

- Add liveness endpoint (#127)

### 🐛 Bug Fixes

- Target set after arch/os
- Bin path needs target
- Release conditional on PR message

### ⚙️ Miscellaneous Tasks

- Release (#128)

## [0.3.0] - 2023-09-19

### 🚀 Features

- Add initial implementation of Kubo RPC API
- Add support for pubsub/* HTTP endpoints
- Add pin endpoints
- Add block endpoints
- Adds id endpoint and adds dag-jose resolving support
- Adds eye command
- Add /metrics endpoint
- *(event)* Add event (commit) libraries for creating events for ceramic
- Add AHash and Recon
- Add necessary fixes for keramik usage
- Implement libp2p Recon protocol
- Serialize eventid
- Add ceramic peer discovery
- Recon-bytes
- Add openapi implementation of events api
- Add offset/limit to subscribe endpoint
- Add sort-key in path
- Add eventId cid parsing
- Add synchronization of interest ranges
- Api subscribe now creates an interest
- Upgrade Recon protocol to honor interest ranges
- Sqlite durability
- Separator from "sort_key|sort_key"
- Recon kilo test fixes
- Msg-size
- Dapp functionality
- Add missing kubo endpoints for import and version
- Use debian image
- Adjustments for js-ceramic tests
- Add version endpoint to ceramic api server
- Add switch to disable/enable Recon
- Release workflow
- Msg-size
- Perform release (#121)
- Release by creating a PR to create a tag, that when merged triggers a release (#123)
- Merge-from-sqlite

### 🐛 Bug Fixes

- Fix all clippy errors
- Require docs and no warnings
- Update 'get' to resolve paths
- Add run target to makefile
- Do not add bootstrap peers
- Use aws creds to login to ecr
- Add use to test case that has many needed types
- Merge errors
- Remove cspell.json
- Work correctly with http client
- Fixes from PR review
- Add tests for recon libp2p
- Fix tests and clippy warnings
- Fmt
- Update lalrpop-util types
- Remove use of cbor, simplify exposing lalrpop in testing
- Address PR review feedback
- Regex char not allowed, change api names
- Change to underscore for naming
- Sort_key bytes bugs
- Key Bytes max_value
- PRAGMA can't use execute
- Fmt
- Cleaner conn_for_filename
- Format don't add strings
- Add sqlite to image
- Update stream type for all supported types
- Use single sql query to get first and last
- Make signer send and allow jwk to be cloned
- Wrap returned peers in "Peers" key
- Release not releases
- Add protoc to release step
- Cache full
- Grab artifacts from artifacts path
- Debug info for packaging
- Remove cycle in debug output
- Reduce build size
- Usage of args should correctly parse and apply now (#110)
- Change bitswap dial behavior
- Args are hard
- Return None instead of error if block is missing
- Release
- Move cliff correctly
- Cleanup tmp files so they don't show dirty in release
- Just use star for cleanup (#119)
- Return v1 cid when fetching blocks
- Slash (#122)
- Rename workflows and use different action
- Release all not detected
- Make versions match
- Use workspace version and only release ceramic-one
- Lock and remove shallow clone
- Install protoc
- Only release if main and version updated
- Don't release if dep changes
- Verify tag for release
- Can run manually
- Disable skip for now
- Combine tag extraction
- Proper release tag
- Try a pat
- Can only use tgz files
- Should listen to copilot

### 🚜 Refactor

- Moves http logic into a single module
- Break http into multiple modules
- Replace iroh-p2p with ceramic-p2p
- Make Recon generic over keys
- Use RangeOpen instead of Range
- Rename sqlitestore
- Remove mutex locking of Recon
- Update if let into match for readability
- Reworks kubo-rpc as an openapi server
- Move beetle locally

### 📚 Documentation

- Add readme and license

### ⚙️ Miscellaneous Tasks

- Add basic CI workflows
- Add protoc install step
- Update ci to use merge_queue
- Add cargo caching to CI
- Explicitly update all deps
- Update makefile
- Add dependabot config
- Add conventional commit action
- Add dockerfile for running ceramic-one
- Remove stutter in directory names
- Use serde versions from workspace
- Only deny warnings during CI
- Setup docker buildx for Github Actions
- Fix buildx missing load option
- Use 3box fork of beetle
- Update deps
- Update beetle dep
- Use dtolnay rust install action
- Add check-api-server make target
- Update beetle dep to point as main
- Use sccache for better Rust caches
- Release (#125)
- Release (#126)

### Wip

- Got actix web tests working
- Test % put are passing
- All tests passing
- Remove println

<!-- generated by git-cliff -->
