# 1.Algorithm

## 66. Plus One 
主要考虑加1等于10时，需要进一位
~~~
class Solution:
    def plusOne(self, digits: List[int]) -> List[int]:
        result = []
        num = 1
        for i in range(len(digits)-1, -1,-1):
            t = digits[i] +  num
            if t == 10:
                t = 0
                num = 1
            else:
                num = 0
            result.insert(0,t)
        if num:
            result.insert(0,num)
        return result
~~~

# 2.Review --[Java字节码介绍](https://dzone.com/articles/introduction-to-java-bytecode)
    专栏推荐的文章

# 3.Tips
    利用Feign调用Restful接口时，需要把从前端请求当前服务的header传递给下一个请求。方法：实现feign.RequestInterceptor接口，获取RequestContextHolder中的ServletRequestAttributes，提取header信息，传递给RequestTemplate。
    当hystrix作为熔断器时，其默认使用thread方式，将获取不到RequestContextHolder，需要修改其并发策略。方法：继承HystrixConcurrencyStrategy，将RequestAttributes传递给线程，启动线程时，RequestAttributes重新放置到当前线程的ThreadLocal中。

# 4.Share
    