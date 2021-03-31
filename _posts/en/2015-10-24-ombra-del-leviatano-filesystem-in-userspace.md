---
title:  "All'ombra del Leviatano: Filesystem in Userspace"
lang: en
ref: filesystem-in-userspace
categories: [talks]
tags: []
featured_image: /assets/images/2015-10-24-ombra-del-leviatano-filesystem-in-userspace.png
conference: "Linux Day 2015"
location: Rome
canonical: https://reale.me/linux-day-2015
media:
  slideshare: https://www.slideshare.net/robertoreale/allombra-del-leviatano-filesystem-in-userspace-87942584
  issuu: https://issuu.com/roberto-reale/docs/linux-day-2015
  source: https://github.com/reale/linux-day-2015
---

I offer a brief historical introduction as well as a technical overview of FUSE, an ingenious combination of a userspace interface and kernel code that allows us to implement, effortlessly, a filesystem in userspace. The reference implementation is fully FOSS, being covered by GPL for the kernel part, and by LGPL for the C library.

From a computer-theoretical point of view, through FUSE the Linux kernel draw closer to more “academic”, microkernel-based operating systems, like the Hurd.

A minimal but functional implementation of a toy filesystem is proposed as a working example.
