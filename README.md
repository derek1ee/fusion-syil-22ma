# fusion-syil-22ma

The work done under `newpost-4th` branch has been merged into `main` for 4th axis support.

The post processor will be using inverse-time feed mode for A-axis by default, but can be set to degree-per-minute feed if desired. The post processor will not be using RTCP (rotational tool center point control, `G43.4`, `G43.5`) or feature coordinate system (`G68.2`) since these features are optional and usually not purchased with Syil X7.

| Feature                                  | Notes                          |
| ---------------------------------------- | ------------------------------ |
| 4th axis                                 | Default to `OFF`, turn on via `Use 4th/A-axis` setting in post config |
| Turn on coolant early                    | Coolant on before G0 move      |
| In process probing                       | Uses Renishaw macros           |
| Custom table position                    | Configurable when posting, incl. A-axis      |
| NC passthrough                           |                                |
| In process tool measure & break control  | Configurable via Fusion tool library, manual NC, or enable for all in post                    |
| M7 air blast                             | |
| M10/11 clamp/unclamp code                | For 4th axis |
| Degree-per-minute feed option            | For 4th axis |
