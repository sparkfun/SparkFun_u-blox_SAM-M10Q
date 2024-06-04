Now let's take a closer look at the basic GNSS position example included in the SparkFun u-blox GNSS Arduino Library.

## Example 1 - Position, Velocity, Time

The first example in the library demonstrates initializing the SAM-M10Q (or any other supported u-blox module) and then receiving position, velocity, and time data from the module. Open the example by navigating to <b>'File'</b> < <b>'Examples'</b> < <b>'SparkFun u-blox GNSS v3'</b> < <b>'Example1_PositionVelocityTime'</b>. Select your <b>Board</b> and <b>Port</b> and click <b>'Upload</b>. Once the code finishes uploading, open the [serial monitor](https://learn.sparkfun.com/tutorials/terminal-basics) with the baud set to <b>115200</b>.

For the best results, make sure the SAM-M10Q has a clear view of the open sky. The first time running this example will take ~23 seconds for the module to get a lock onto any satellites. After this initial cold start, the battery on the board will provide power to the hot start circuitry in the module to assist with warm/hot starts during power cycles to drop the time-to-fix down to just one second. This hot start lasts up to four hours between power cycles.
