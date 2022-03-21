---
id: guidelines-inevitable-inconsistency
title: Inevitable Inconsistency
excerpt: Menteca's very own blazing fast consistency model
updated: 1647892975956
created: 1647892975956
---

Inevitable inconsistency is the consistency model of choice in Menteca that
guarantees blazing fast performance regardless of load. It boils down to
updating data immediately without worrying whether or not the result would make
sense at all. Since it's a performance-centric model, inevitable inconsistency
greatly favors speed over correctness.

There is no single way to achieve inevitable inconsistency. The most popular
approach involves using cached data with questionable validity (preferably
without any TTL) and blindly overriding entire chunks of data in parallel.