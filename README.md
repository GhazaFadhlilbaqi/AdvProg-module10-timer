# Advanced Programming Module 10 - Timer Future
### Muhammad Ghaza Fadhlilbaqi - 2306173321

## Understanding how it works
![](images/experiment1.png)
The newly added message that was placed under the spawner is **printed first**, before the print statements inside the spawner above it. This happens because the first two prints are placed in an ```async``` function that is called by the spawner. The spawner is a process that is running in the background and does not halt the main process, so the main function can just proceed to the next instruction, which in this case, is printing the newly added message.

## Multiple Spawn and removing drop
![](images/experiment2.png)
When the ```drop statement``` is removed, the program won't end after printing all the messages within the spawners. The executor basically waits for more tasks to run since ```drop``` is never called. So the ```drop``` function is basically a way to tell the executor that all of the tasks have been run, and that it can stop.
