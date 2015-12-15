---
layout: blog
title: Prune those branches
---

Remember to prune old branches that are no longer present in the remote repository.

```
git fetch --prune
```

Also, if you forget how to remove a remote branch:

```
git branch -r -d ${BRANCH_NAME}
```

Or, if you learned before the `-r` parameter was added:

```
git push origin :${BRANCH_NAME}
```

Which means, 'push nothing into this remote branch'.
