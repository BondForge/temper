# Controlled utilities

BEM-based component classes are the default. Utilities are narrow exceptions for genuinely cross-component concerns.

Rules: prefix with `u-`; define centrally; require demonstrated reuse and review; do not use utility chains to build 
component appearance; avoid specificity escalation and `!important` as routine override mechanisms.

**Candidate utilities (not automatically approved in every project):**

| Class | Purpose | Caution |
| --- | --- | --- |
| `u-sr-only` | Visually hidden, accessible text | Do not hide from assistive tech |
| `u-hidden` | Fully hidden | Prefer native `hidden` when appropriate |
| `u-text-center` | Exceptional cross-component alignment | Prefer component rules for normal variants |
| `u-clearfix` | Legacy floats | Prefer `flow-root`, Grid, or Flexbox for new layouts |

Only use a utility once the adopting project has defined and approved it. Utility-first frameworks are not Temper's 
default; adopting one is an explicit architecture decision.
