


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #是返回函数
    def count1():
        fs = []
        for i in range(1, 4):
            def f():
                 return i*i
            fs.append(f)
        return fs
    f1, f2, f3= count1()
    print(f1(), f2(), f3())
    #不是返回函数
    def count2():
        fs = []
        for i in range(1, 4):
            def f():
                 return i*i
            fs.append(f())
        return fs
    print(count2())