# kypo-demo

A simple sandbox with a Telnet server and client with training definition for testing purposes.

## Usage

1. In KYPO > Sandboxes > Definition create a new definition with URL of: this repository > Clone > Clone with SSH and Revision: last commit SHA
2. In Sandboxes > Pool create a new pool with the Sandbox Definition (telnet-server-sandbox)
3. Allocate the sandbox and wait until each Allocation Request Stages finishes
4. In Trainings > Definition upload the [training.json](./training.json)
5. In Trainings > Instance create and continue editing a new instance
6. Assing the pool from step 3. to the training instance
7. Copy access token from the training instance and use it in Trainings > Run
8. Follow instructions in the run
