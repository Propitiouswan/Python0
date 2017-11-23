


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    from types import MethodType
    #定义class
    class Student(object):
        pass
    #给实例1绑定属性
    instance1 = Student()
    instance1.name = 'wanjun'
    print(instance1.name)
    #定义一个函数作为实例方法
    def setage(self, age):
        self.age = age
    #给实例2绑定方法,方法对实例1不起作用
    instance2 = Student()
    instance2.setage = MethodType(setage, instance2)
    instance2.setage(25)
    print(instance2.age)
    #给class绑定方法,方法对所有实例起作用
    def setscore(self, score):
        self.score = score
    Student.setscore = setscore
    instance1.setscore(1)
    print(instance1.score)
    instance2.setscore(2)
    print(instance2.score)