---
title: "SSH Key: How To Solve Permissions 0644 for 'file.pub' are too open"
description:
date: 2024-09-29T21:18:09-04:00
image:
math:
# license:
# hidden: false
comments: true
draft: false
tags:
  - ssh key

categories:
  - debugging
---

<br><br>

I wrote the host infomation to ./ssh/config:

```
Host arbitrary-name
  HostName 133.125.85.79
  User user-name
  IdentityFile location-of-secret-key
```

But I got this error:

```
But I got this eeror :Permissions 0644 for 'secret-key.pub' are too open.
```

To fix this, I run this command on terminal.

```
chmod 400 ~/.ssh/secret-key
```

And after run this command, it works!
