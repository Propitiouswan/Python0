

    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    # This is a solution to Hanoi Tower.
    def move(n, a, b, c):
        if n == 1:
            print(a,'→',c)
        else:
            move(n-1, a, c, b)
            move(1, a, b, c)
            move(n-1, b, a, c)
    move(3, 'A', 'B', 'C')