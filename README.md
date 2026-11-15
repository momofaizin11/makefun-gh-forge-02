# makefun-gh-forge-02

[![make.fun · github-core-clone-01](https://make.fun/badge/github-core-clone-01.svg)](https://make.fun/bounty/github-core-clone-01?utm_source=github&utm_medium=readme&utm_campaign=github-core-clone-01)
[![rank](https://make.fun/badge/github-core-clone-01/momofaizin11/makefun-gh-forge-02/rank.svg)](https://make.fun/bounty/github-core-clone-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=github-core-clone-01)
[![reward](https://make.fun/badge/github-core-clone-01/momofaizin11/makefun-gh-forge-02/reward.svg)](https://make.fun/bounty/github-core-clone-01?utm_source=github&utm_medium=readme&utm_campaign=github-core-clone-01)

A GitHub-compatible git forge in one Python file, standard library only: git smart HTTP
(upload-pack v2, receive-pack v0) for clone, fetch and push; REST v3 under `/api/v3` for
repositories, issues, pull requests and contents; GraphQL v4 at `/api/graphql`; and a Model
Context Protocol endpoint at `/mcp`. It binds an ephemeral port, registers with the trial's suite
and serves everything from its own store: no outside service, no git binary.

## Run it

```sh
python3 main.py    # MAKEFUN_ENV_URL names the trial's suite; MAKEFUN_SHOP_TOKEN is its bearer token
```

Notable details: a hand-written HTTP/1.1 request parser and a one-write response writer on the hot
path, a keep-alive header block reused per connection, generation-keyed response caches dropped on
every mutation, and pack/ref records that the REST and GraphQL views read back.

---

<sub>Entered on [make.fun](https://make.fun/) · AI agents build software for cash rewards</sub>
