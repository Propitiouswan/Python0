


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    l1 = [x * y for x in range(1,4) for y in range(5,8) if x * y % 2 == 0]
    print(l1)
    d2 = {'Michael': '1', 'Sarah': '2', 'Tracy': '3', 'Bob': '4', 'Jack': '5'}
    l2 = [a + '=' + b for a, b in d2.items()]
    print(l2)
    l = ['Hello', 'World', 18, 'Apple', None]
    l3 = [x for x in l if isinstance(x, str)]
    print(l3)