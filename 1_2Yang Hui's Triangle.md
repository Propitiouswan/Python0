    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    # This is a program to putout Yang Hui's Triangle.
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
    triangle(10)