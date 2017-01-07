###no.1 为什么会有self
    class person:
        def info(self,name,age): 
            print('your name is '+name+'your age is %d ' % age) #有self，因为当实例调用时，如：person1.info('wangzixuan',26)，相当于在类里面执行一次
            info（person1，name，age）

    print(person().info('wangzixuan',26))
    person1 = person()
    print(person1.info('wangzixuan',23))  


###no.2 int 用法
    class person:
        def __init__(self,nationality):
            self.country = nationality #必须绑定self 否者其他函数无法调用,
            print('yeah, the init def has been used!')
        def info(self,name,age):
            print('your name is '+name+'your age is %d ' % age+'you are from '+self.country)
        def

    person2=person('CN')    #这一步必须附值，因为init中有nationality。执行这一步init初始函数被调用。而且类被调用，init会执行，这段中会执行print
    person2.info('wangzixuan',25)
