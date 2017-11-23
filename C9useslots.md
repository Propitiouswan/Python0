


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #为了达到限制的目的，Python允许在定义class的时候，定义一个特殊的__slots__变量，来限制该class实例能添加的属性。
    #使用__slots__
    class Student(object):
        __slots__ = ('name', 'age')
    s1 = Student()
    s1.name = 'Propitiouswan'
    s1.age = 21
    print(s1.name, s1.age)
    #s1.score = 100
    class Substudent(Student):
        __slots__ = ('score')
    s2 = Substudent()
    s2.name = 'WenhuiZhou'
    s2.age = '22'
    s2.score = '100分'
    print(s2.name, s2.age, s2.score)