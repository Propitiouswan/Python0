


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #回数是指从左向右读和从右向左读都是一样的数，例如12321，909。利用filter()滤掉10000以内非回数。
    def naturalnum():
        n = 0
        while True:
            yield n
            n = n + 1
    def divisible(x):
        x = str(x)
        n = 0
        a = 0
        b = len(x) - 1
        while 2 * n < len(x) + 1 and x[a] == x[b]:
            a = a + 1
            b = b - 1
            n = n + 1
        return 2 * n >= len(x)
    def plalindrome():
        it = naturalnum()
        while True:
            it = filter(divisible, it)
            n = next(it)
            yield n
    for x in plalindrome():
        if x < 10000:
            print(x)
        else:
            break