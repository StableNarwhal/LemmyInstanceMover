
# Lemmy Instance Mover

This web application exports your user data (community follows, blocklists, profile settings) and (optionally) imports them to the target account.


**How this works:**



1. Input your instances, usernames and passwords and optionally 2FA-Tokens.

2. The clientside JavaScript code processes your inputs locally and tries to grab a special token using your provided export instance, username and password.

3. If the export token can be grabbed, it gets used to authenticate a request to grab your user data from your export instance.

4. If the userdata export was successful, another special token is attempted to be grabbed, this time from your provided import instance.

5. If the import token can be grabbed, another request to upload your user data to your import instance is attempted.

**At this point, if the log is all green, the process is complete. You can safely close the window, your sensitive input and local user data gets deleted.**

![overview_compact](https://github.com/StableNarwhal/LemmyInstanceMover/assets/14216536/7f2fcf24-cd34-48d1-be74-5957b024962c)
