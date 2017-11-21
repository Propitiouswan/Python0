    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #reduce(f, [x1, x2, x3, x4]) = f(f(f(x1, x2), x3), x4)
    from functools import reduce
    def numtoint(x, y):
        if x is None:
            return y
        elif y is None:
            return x
        else:
            x = 10 * x + y
            return x
    def chartonum(x):
        d = {'0': 0, '1': 1, '2': 2, '3': 3, '4': 4, '5': 5, '6': 6, '7': 7, '8': 8, '9': 9}
        if x in d:
            return d[x]
        else:
            pass
    def inttofloat(x, n):
        while n:
            x = x / 10
            n = n - 1
        return x
    #convert str to int
    a = reduce(numtoint, map(chartonum, '234567'))
    print(a, type(a))
    #convert str to float
    b = '234.567'
    n=len(b)
    c = reduce(numtoint, map(chartonum, b))
    print(c, type(c))
    for x in b:
        n = n - 1
        if not(x == '.'):
            pass
        else:
            break
    print(n)
    d = inttofloat(c, n)
    print(d)