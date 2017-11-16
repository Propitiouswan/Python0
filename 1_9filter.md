


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #filter()把传入的函数依次作用于每个元素，然后根据返回值是True还是False决定保留还是丢弃该元素。
    #取1000以内素数
    def odditer():
        n = 1
        while True:
            n = n + 2
            yield n
    def divisible(n):
        return lambda x: x % n > 0
    def prime():
        yield 2
        it = odditer()
        while True:
            n = next(it)
            yield n
            it = filter(divisible(n),it)
    for x in prime():
        if x < 1000:
            print(x)
        else:
            break