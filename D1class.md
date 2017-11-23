


    #!/usr/bin/env python3
    # -*- coding: utf-8 -*-
    #在绑定属性时，如果我们直接把属性暴露出去，虽然写起来很简单，但是，没办法检查参数，导致可以把成绩随便改。
    class Student(object):
        def set_score(self, score):
            if not isinstance(score, int):
                print('请输入整数。')
            elif score < 0 or score > 100:
                raise ValueError('请输入0~100之间的数。')
            else:
                self._score = score
        def get_score(self):
            return self._score
    s1 = Student()
    s1.set_score(56)
    print(s1.get_score())