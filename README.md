# fusion-syil-22ma

On 6/14/2023, Autodesk made a major update/rewrite to the Syil/Syntec post processor, in their words, `updated syil syntec post to use shared content across post processors.`

The main branch, which has been under development before this change, is still based on the old post, up to version `44013`.

A new branch, `newpost-4th` is introduced to work on the support for 4th axis, and is based on the new version of the post.

| Branch      | Description          |
| ----------- | -------------------- |
| main        | Based on 44013       |
| newpost-4th | Based on 44083       |

The development has been paused for `main` branch, and active development is underway for `newpost-4th` branch.

The `newpost-4th` branch is still experimental, and not all the improvements/modification in the main branch have been ported to it. `newpost-4th` will be merged into `main` when the development for 4th axis support is stable, and after all the improvements have been ported over.

The post processor will be using inverse-time feed mode for A-axis by default, but can be set to degree-per-minute feed if desired. The post processor will not be using RTCP (rotational tool center point control, `G43.4`, `G43.5`) or feature coordinate system (`G68.2`) since these features are optional and usually not purchased with Syil X7.

| Feature                                  | `main` | `newpost-4th` |
| ---------------------------------------- | ------ | ------------- |
| 4th axis                                 | no     | in progress   |
| Turn on coolant early                    | yes    | no            |
| In process probing                       | yes    | yes           |
| Custom table position                    | yes    | yes (incl. A-axis) |
| NC passthrough                           | yes    | yes           |
| In process tool measure & break control  | yes    | yes           |
| M7 air blast                             | yes    | yes           |
| M10/11 clamp/unclamp code                | no     | yes           |
| Degree-per-minute feed option            | no     | yes           |
