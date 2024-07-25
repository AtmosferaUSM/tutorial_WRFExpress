# Steps To Monitor and Troubleshoot

You can check the progress by opening another shell and typing `squeue` in the terminal. You can see the progress when the model has started running.

## Monitoring the Model

1. Open another shell on the AWS ParallelCluster page.
2. Navigate to `/shared/scratch/WRF/run`.

## Troubleshooting Errors

If there is an error, type `tail rsl.error.0000` to show the error message.
