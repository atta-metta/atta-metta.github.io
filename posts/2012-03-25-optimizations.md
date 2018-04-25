published_date: 2012-03-25 00:00:00 +0300
title: Optimizations
categories:
    - metta
    - llvm
    - sse
---
The reason for not booting was simple - Clang, seeing that target is Pentium 4 and above, optimized some memmoves into SSE operations. Bochs didn't expect that.

Now everything boots up until exceptions, at which point I believe the `__builtin_longjmp` primitive fails. Debugging it.