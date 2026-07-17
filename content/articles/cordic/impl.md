---
draft : false
title : "A pythonic implementation of the CORDIC algorithm"
toc: true
prev: impl
next: presentation
cascade:
    type: docs
---

```python {filename="hello.py"}
import numpy as np

def cordic_angles(target_angle, iterations=16):
        remaining = target_angle

        rotations = []

        K = 1.0

        for i in range(iterations):
            angle = np.degrees(np.atan(2 ** -i))

            if remaining >= 0:
                rotations.append(angle)
                remaining -= angle
            else:
                rotations.append(-angle)
                remaining += angle

            K *= 1 / np.sqrt(1 + 2 ** (-2 * i))

        return (rotations, K, remaining)

```