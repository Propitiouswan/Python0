


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    # List, tuple and dict are iterable.
    l = ['Michael', 'Sarah', 'Tracy', 'Bob', 'Jack']
    t = ('Michael', 'Sarah', 'Tracy', 'Bob', 'Jack')
    d = {'Michael': 1, 'Sarah': 2, 'Tracy': 3, 'Bob': 4, 'Jack': 5}
    #列表迭代
    for x in l:
        print(x)
    #元组迭代
    for x in t:
        print(x)
    #字典迭代
    for x in d:
        print(x)
    for x in d.values():
        print(x)
    for x, y in d.items():
        print(x, y)
    #判断是否可迭代
    from collections import Iterable
    a = isinstance('ABCD', Iterable)
    print(a)
    a = isinstance(l, Iterable)
    print(a)
    a = isinstance(t,Iterable)
    print(a)
    a = isinstance(d,Iterable)
    print(a)
    #给list加索引号
    for i, x in enumerate(l):
        print(i, x)`enter code here`