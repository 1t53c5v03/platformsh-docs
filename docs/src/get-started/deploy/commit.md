---
title: Git commit
weight: -9
description: Start getting your project into Platform.sh.
---

Once you have your project initialized, it's time to add the basics to get it deployed.

Create a file to hold your app configuration:

```bash
touch .platform.app.yaml
```

This file holds all the configuration for the container where your app lives.
By keeping the configuration in this file,
you ensure it remains the same across all environments, from development to production.

Add basic properties for your app, such as its name and language:

{{% get-started/basic-app %}}

{{% get-started/build-hook %}}

Commit your changes (to save your changes):

```bash
git commit -m "Add Platform.sh files"
```

Push your changes (to share your changes with everyone with access to your project/repository):

```bash
platform push
```

{{% get-started/service-needed %}}

{{< get-started/next-button next="/get-started/add-data/branch.html" nextText="I'm ready to branch" >}}
