


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #请用匿名函数改造下面的代码。
    def is_odd(n):
        return n % 2 == 1
    L1 = list(filter(is_odd, range(1, 20)))
    print(L1)
    L2 = list(filter(lambda x : x % 2 ==1, range(1, 20)))
    print(L2)a`enter code here`