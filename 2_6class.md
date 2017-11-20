


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    class MyClass:
        i = 123
        def f(self):
            return 'hello world'
    print(MyClass.i)
    t = MyClass()
    print(t.f(), MyClass.f(MyClass))