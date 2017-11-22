


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #数据封装
    class Student(object):
        def __init__(self, name, score):
            self.name = name
            self.score = score
        def get_grade(self):
            if self.score >= 90:
                return 'A'
            elif self.score >= 60:
                return 'B'
            else:
                return 'C'
    instance1 = Student('WenhuiZhou', 100)
    instance2 = Student('Propitiouswan', 78)
    instance3 = Student('WenhuiZhou', 59)
    print(instance1.name, instance1.get_grade())
    print(instance2.name, instance2.get_grade())
    print(instance3.name, instance3.get_grade())