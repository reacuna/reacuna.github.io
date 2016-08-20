---
title: Fragments and the Delegate Pattern
---

It seems to me that when doing Android development, it might be a good idea to
avoid the delegate pattern to communicate between the fragment and the activity
that contains it.

This is because fragments and activities can be destroyed and recreated several
times.


