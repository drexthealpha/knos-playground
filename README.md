# knos-playground

Try [Knos](https://github.com/drexthealpha/Knos) from both sides with a GitHub account and nothing else. Nothing is
installed, and no wallet is needed.

**Fund a test task.** [Open the issue](https://github.com/drexthealpha/knos-playground/issues/new?template=fund-a-test-task.md)
and press **Submit new issue**. Its text holds the line `/knos fund 5 checks: none auto`: 5 test USDC from the devnet faucet go into an
escrow on Solana for that issue, and Knos answers in a comment.

**Take one.** Pick an [open issue](https://github.com/drexthealpha/knos-playground/issues),
[edit `words.py`](https://github.com/drexthealpha/knos-playground/edit/main/words.py) in the browser so that it prints the
words of a line in reverse order, and open the pull request with `Closes #<the issue's number>` in its description.
The checks in `.knos/acceptance/<number>/` run your file as a separate process and compare what it prints. When every
answer matches, GitHub signs that it did and the escrow pays you: to the wallet you bound, or held for your account
until you bind one. Nobody merges and nobody decides.

**Take a funded task.** Issues labelled [`knos-funded`](https://github.com/drexthealpha/knos-playground/issues?q=is%3Aissue+is%3Aopen+label%3Aknos-funded)
are small programming tasks, each with its own file under `tasks/`. Edit that file, try it with
`python3 check.py <task>`, and open the pull request with `Closes #<the issue's number>`. A maintainer merges a pull
request that passes the check, and the merge pays your account. Test USDC, no monetary value.

The limits: an issue is funded only as it is opened, with at most 5 test USDC; one account funds at most 3
in a day (UTC); the faucet serves this repository once a minute; issues 1 to 200 have checks. A first pull request
from an account that is new to GitHub waits until a maintainer lets its check run.

It is test money: the faucet mints it, nobody can withdraw it from the faucet's balance, and it is worth nothing.
What is counted, and how: [docs/PLAYGROUND.md](https://github.com/drexthealpha/Knos/blob/main/docs/PLAYGROUND.md).

On Solana devnet today, in test USDC.
