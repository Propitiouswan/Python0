


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #定义类
    class Student(object):
        a = 123
        def grade(self, number):
            return number
        def __init__(self, name, score):
            self.name = name
            self.score = score
    #创建实例
    instance1 = Student('Propitiouswan', 100)
    instance2 = Student('WenhuiZhou', 99)
    #应用
    print(instance1.a)
    t = instance1.grade(9)
    print(t)
    print(instance1.name, instance1.score)
    print('=' * 30)
    print(instance2.a)
    t = instance2.grade(6)
    print(t)
    print(instance2.name, instance2.score)