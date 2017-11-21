
#!/usr/bin/env python3
# -*- coding: utf-8 -*-
# Generator is iterable.
g1 = (x * x for x in range(0,6))
a1 = next(g1)
a1 = next(g1)
print(a1)
for a1 in g1:
    print(a1)
def triangle():
    x = 0
    L = []
    while x < 10:
        if x == 0 or x == 1:
            pass
        else:
            y = x - 1
            while y:
                L[y] = L[y] + L[y - 1]
                y = y - 1
        L.append(1)
        x = x + 1
        yield L
    return 'WANJUN'
g2 = triangle()
while True:
    try:
        a2 = next(g2)
        print(a2)
    except StopIteration as x:
        print(x)
        break`enter code here`