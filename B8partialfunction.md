


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #偏函数可以通过设定参数的默认值，降低函数调用的难度。
    x1 = int('15', 8)
    print('x1 =', x1)
    x2 = int('15', 16)
    print('x2 =', x2)
    def int2(x, base=2):
        return int(x, base)
    x3 = int2('1100')
    print('x3 =', x3)
    #偏函数
    import functools
    #1
    int2_1 = functools.partial(int, base=2)
    x4 = int2_1('1100')
    print('x4 =', x4)
    #2
    kw = { 'base': 2 }
    int2_2 = functools.partial(int, **kw)
    x5 = int2_2('1100')
    print('x5 =', x5)
    #3
    max2 = functools.partial(max, 10)
    x6 = max2(5, 6, 2)
    print('x6 =', x6)