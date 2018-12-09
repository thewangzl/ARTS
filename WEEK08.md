#1.Algorithm
##38. Count and Say
~~~
class Solution:
    def countAndSay(self, n):
        """
        :type n: int
        :rtype: str
        """
        ret = ""
        if n == 1:
            ret = "1"
        else:
            t = self.countAndSay(n -1)
            nums = 0
            index = 0
            for index in range(len(t)):
                nums+= 1
                if index + 1 == len(t) or t[index] != t[index + 1] :
                    ret += str(nums) + t[index]
                    nums = 0
        return ret
~~~

#2.Review --[How to Write a Technical Specification or Software Design Document (SDD)](https://blog.nuclino.com/how-to-write-a-technical-specification-or-software-design-document-sdd)
    The real goal of writing a software design document is to force you to really think through the design
    and gather feedback from your team,allowing you to thoroughly evaluate your project before you waste
    a bunch of time implementing the wrong solution or the solution to the wrong problem.
    A detailed and thorough design document remains the most useful tool for making sure the right work 
    gets done.
    the document contains some sections:Title and people、Overview、Context、Goal、Milestones、Current solution、Proposed solution、Alternative solutions、Discussion、Scope and timeline.
    The ways to make the experience more engaging:Don't write it in Word、Keep it simpe、Make it visual with charts and diagrams、Do the "vacation test"、Do the "skeptic test".
    a few final tips to help you make the most of your time and efforts:Get everyone involved、Gather feedback early、Don't afraid to prototype、Address all points of contention、Treat the SDD as a living document.

    
#3.Tips
    用nginx做反向代理时，如果监听端口不是80,proxy_set_header Host 应该设置为$host:$server_port。否则，java应用中有response.setRedirect时，URL会直接变为80端口，不在原来的端口上，导致出错。
    $server_port 为nginx监听的端口；
    $proxy_port 为服务器真正访问的端口。

#4.Share
    [A/B测试的数学原理与深入理解​​​​](https://mp.weixin.qq.com/s/2AHnBb55TnEq2A73adY-0w)