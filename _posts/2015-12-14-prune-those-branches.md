---
layout: blog
title: Prune those branches
---

Remember to prune old branches that are no longer present in the remote repository.

```bash
git fetch --prune
```

And delete the branch on the remote:

```bash
git push origin :${BRANCH_NAME}
```

Which means, 'push nothing into this remote branch'.
