


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    class Myobject(object):
        def __len__(self):
            return 90
        def __init__(self):
            self.x = 100
        def power(self):
            return(self.x * self.x)
    obj = Myobject()
    print(obj.__len__())
    print(hasattr(obj, 'x'))
    print(obj.x)
    print(hasattr(obj, 'y'))
    setattr(obj, 'y', 50)
    print(hasattr(obj, 'y'))
    print(obj.y)
    print(getattr(obj, 'z', 404))
    print(hasattr(obj, 'power'))
    fn = getattr(obj, 'power')
    a1 = obj.power()
    a2 = fn()
    print(a1, a2)