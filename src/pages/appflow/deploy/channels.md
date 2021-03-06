---
title: 'Channels'
previousText: 'Live Update Builds'
previousUrl: '/docs/appflow/deploy/builds'
nextText: 'Differentials'
nextUrl: '/docs/appflow/deploy/differentials'
---

A channel points to a specific Live Update build of your app that will be shared with any devices configured to
listen to that channel for updates. You can change the build a channel points to whenever you'd like, and can rollback changes as well.

When you [install the Appflow SDK](/docs/appflow/quickstart/installation) in your app
(by clicking Install Instructions on a channel), any native binary configured to that channel
will check the channel for available updates whenever it is loaded.

## Setting up a Channel

Every app comes with two default channels: **Master**, and **Production**.

Common use cases are using a **Production** Channel for your App Store binaries, and the **Master**
channel to run a native binary on your phone during development that gets automatically updated.

Once you've set up a Channel, just click **Install Instructions** next to that Channel and it will walk you
through the options available and generate the Command Line command that you should run.

To create new channels beyond these two, you must have a paid Ionic Appflow membership. To add new channels,
simply view the channels list by going to Deploy -> Destinations, and then click the `New destination` button.


## Assigning a Build to a Channel

Once you have created a Channel, go back to the **Builds** section of your app.
On the right side of each Build, you'll see a "Deploy live updates" button.

![Assign build to a channel](/docs/assets/img/appflow/assign-to-channel.png)

Click this to set the Build as active for a Channel.

Once a Build is set as active for a Channel any native binaries that have been set up with Ionic Live Update
for this Channel will receive the new update next time they check in.

## Automating Deployment from a Git Branch

If your interested in automating your deploys from git push all the way to deploying to a channel you can
take advantage or our [Automation](/docs/appflow/automation/intro) features if your [plan](/pricing) includes them.
