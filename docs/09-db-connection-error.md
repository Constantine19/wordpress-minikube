## Problem

When connecting to WordPress url, it will show that there is an error establishing a database connection.

![1](./images/07%20-db-connection-error.png)


## Solution

Checked the pod status and there was indeed the problem with starting the pod itself. This was due to the fact that I was deploying on Mac with M1 chip and the image used for mysql is outdated.

The solution was to switch an image version from `mysql:5.6` to `mysql:8.0`.
