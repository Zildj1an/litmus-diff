# Litmus-RT Patch

This patch was generated using LITMUS-RT [source code](), comparing its
most recent version to its kernel base (v4.9):

```
$ git diff db3fd4527ed32be44cbd8ffa6dd6a301c89d0d6d 7811e5b1eaef361f45659a1f6d49acb050b1f316 > litmus.patch
```

these two commits are:

```
$ git log
commit 7811e5b1eaef361f45659a1f6d49acb050b1f316 (HEAD -> linux-4.9-litmus, origin/linux-4.9-litmus, origin/HEAD)
Author: Samuel Tardieu <sam@rfc1149.net>
Date:   Thu Jan 21 18:50:56 2021 +0100

    Add missing include

    Structures in include/litmus/reservations/reservation.h use the
    lt_t type which is defined in litmus/rt_param.h. This header must
    be included so that reservation.h can be included without, or before
    an explicit inclusion of litmus/rt_param.h.

(...)


commit db3fd4527ed32be44cbd8ffa6dd6a301c89d0d6d (HEAD -> linux-4.9-litmus)
Author: Greg Kroah-Hartman <gregkh@linuxfoundation.org>
Date:   Thu May 25 15:45:05 2017 +0200

    Linux 4.9.30
```

## How big is this patch?

We can see that 105 files are modified by the patch. With the command wc we
get the total size:

```
$ wc litmus.patch 
 20688  76495 558654 litmus.patch
```
