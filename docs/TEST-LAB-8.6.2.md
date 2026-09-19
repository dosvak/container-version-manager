# Container Version Manager - deep test

29/29 checks passed (2026-09-19 17:17)

| Section | Check | Result | Detail |
|---|---|---|---|
| Containers | Lookup lists process applications and toolkits | PASS | Info: 48 container(s) of 48 / 15 rows |
| Containers | kind filter = toolkits only | PASS | 15 rows |
| Containers | text filter narrows to the containers mentioning Triage | PASS | ['FTRIAGE Failed Instance Triage process app no Main 2026-09-19 16:44:42 celladmin Failed Instance Triage - the failed process instances of the server grouped by error signature (application, process, s', 'TRGSMP Triage Sample process app no Main 2026-09-19 15:48:23 celladmin Triage Sample - test fi |
| Containers | Orphaned toolkit snapshots listed | PASS | Info: 1 orphaned toolkit snapshot(s) (no process app or toolkit depends on them) / ['BAWJSN BAW JSON 1.0 M'] |
| Containers | Restore of the archived container CRAI | PASS | Success: 1 of 1 container(s) restored / ['CRAI Custom REST API Integration process app no Main 2026-09-06 08:59:03 celladmin'] |
| Containers | Archive of CRAI again | PASS | Success: 1 of 1 container(s) archived / ['CRAI Custom REST API Integration process app yes Main 2026-09-06 08:59:03 celladmin'] |
| Snapshots | Snapshots of container switches the tab and lists named snapshots + tip | PASS | Info: 3 snapshot(s) of Triage Sample (TRGSMP) / 3 rows |
| Snapshots | Details shows snapshot, environment variables, EPVs and team bindings | PASS | Snapshot 1.1 (1.1) of TRGSMP Snapshot, environment variables, exposed process values, team bindings (JSON) CloseOK |
| Snapshots | Deactivate 1.0 succeeds (active = no) | PASS | Success: 1 of 1 snapshot(s) deactivated / ['1.0 1.0 Main no no no New no Standard 2026-09-19 15:48:23 celladmin Operations CP4BA 1.0'] |
| Snapshots | Activate 1.0 succeeds (active = yes) | PASS | Success: 1 of 1 snapshot(s) activated / ['1.0 1.0 Main no yes no New no Standard 2026-09-19 15:48:23 celladmin Operations CP4BA 1.0'] |
| Snapshots | Make default 1.1 (a Workflow Server operation; a Process Center may refuse it) | PASS | Error: 0 of 1 snapshot(s) make_defaultd - refused: 1.1: CWTBG0688E: This action can be performed only on a workflow server. / ['1.1 1.1 Main no yes no New no Standard 2026-09-19 16:04:23 celladmin Triage Sample 1.1'] |
| Snapshots | Export CSV (snapshots) | PASS |  |
| Snapshots | Delete unnamed snapshots asks for confirmation | PASS | Delete the unnamed snapshots of TRGSMP beyond the kept number / older than the date (Workflow Center only)? The deletion |
| Snapshots | unnamed snapshot cleanup is accepted and queued (Queue tab) | PASS | Success: unnamed snapshot cleanup of TRGSMP accepted - operation running (last change 2026-09-19 21:14:10) - refresh the status until it finishes / https://localhost:9443/ops/system/queue/161?key=234a3e51418cd1efcfac69b8e3855abe |
| Queue | queued cleanup finishes (failure "nothing to delete" is the expected answer with kept number 5) | PASS | Status  Info: operation failure (last change 2026-09-19 21:14:10) - finished: The keptNumber is greater than the number of found snapshots, nothing to delete |
| Variables | environment variables of TLIST / 1.0 listed | PASS | Info: 14 environment variable(s), 0 EPV value(s) of TLIST / 1.0 / 14 rows |
| Variables | row selection fills the editor | PASS | appTitle = Task Lists (dbg) |
| Variables | Set value updates the variable on the server and the list refreshes | PASS | Success: appTitle = Task Lists (dbg) (CVMGR test) set on TLIST / 1.0 (the running snapshot reads the / ['appTitle Task Lists (dbg) (CVMGR test)'] |
| Variables | original value restored | PASS |  |
| Variables | Export CSV (variables) | PASS |  |
| Cleanup | Count instances (terminated, one application) | PASS | Info: 0 instance(s) in state terminated of TRGSMP |
| Cleanup | Delete instances asks for confirmation | PASS | Delete the instances in the selected states of TRGSMP? This cannot be undone; the deletion is queued on the server. Canc |
| Cleanup | instance deletion accepted (the accepted request answers a count URL, shown on the Queue tab) | PASS | Success: deletion of the terminated instances of TRGSMP accepted - GET /std/bpm/processes/count -> { "count": 0 } / https://localhost:9443/ops/std/bpm/processes/count?containers=TRGSMP&states=terminated |
| Queue | the URL of the accepted deletion is refreshed (instance count after the deletion) | PASS | Status  Info: GET /std/bpm/processes/count -> { "count": 0 } |
| Cleanup | count after the deletion is 0 | PASS | Info: 0 instance(s) in state terminated of TRGSMP |
| Cleanup | Delete closed tasks: accepted on BAW 24 / CP4BA, a clear error on 8.6.2 (no /std/bpm/tasks) | PASS | Error: closed-task cleanup of TRGSMP refused: HTTP 404 |
| Cleanup | Resume suspended instances is accepted (queued) | PASS | Success: resume of the suspended instances of TRGSMP / 1.1 accepted - operation success (last change 2026-09-19 21:16:45) - finished |
| all | no JavaScript errors | PASS | [] |
| all | no failed HTTP calls of the coach | PASS | [] |

