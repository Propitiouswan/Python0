


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #map()函数接收两个参数，一个是函数，一个是Iterable。
    #map将传入的函数依次作用到序列的每个元素，并把结果作为新的Iterator返回。
    def triangle(n):
        x = 0
        L = []
        while x < n:
            if x == 0 or x == 1:
                pass
            else:
                y = x - 1
                while y:
                    L[y] = L[y] + L[y - 1]
                    y = y - 1
            L.append(1)
            x = x + 1
            print(L)
        return L
    a = map(triangle,[x for x in range(1, 6)])
    print(list(a))