

    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #利用闭包返回一个计数器函数，每次调用它返回递增整数。
    def createcounter():
        global n
        n = 0
        def counter():
            global n
            n = n + 1
            return n
        return counter
    
    counterA = createcounter()
    print(counterA(), counterA(), counterA(), counterA(), counterA())
    # 1 2 3 4 5
    counterB = createcounter()
    if [counterB(), counterB(), counterB(), counterB()] == [1, 2, 3, 4]:
        print('测试通过!')
    else:
        print('测试失败!')

