---
title: "Nested Resiliency"
description: "Storage Spaces driver support for 1 node + 1 drive fault tolerance on 2-node S2D clusters."
date: "2018-10-02T00:00:00-08:00"
slug: "nested-resiliency"
info: "https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/nested-resiliency"
tags: [ "Microsoft", "Windows", "S2D", "C", "C++" ]
---

During the development of Windows Server 2019, one of the features that I worked
on at Microsoft was adding Storage Spaces driver support for provisioning,
deploying, and managing Storage Spaces with 1 node + 1 drive fault tolerance.
This feature was desired for 2-node Storage Spaces Direct (S2D) cluster
deployments so that a Storage Space could survive an additional drive failure if
1 of 2 nodes went offline for any reason (e.g., node reboot).
