


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    L = [('Bob', 75), ('Adam', 92), ('Bart', 66), ('Lisa', 88)]
    #按姓名排序
    def byname(t):
        x = t[0]
        return x
    L1 = sorted(L, key=byname)
    print(L1)
    #按分数由高至低排序
    def byscore(t):
        x = t[1]
        return x
    L2 = sorted(L, key=byscore, reverse=True)
    print(L2)