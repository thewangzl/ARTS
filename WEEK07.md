#1.Algorithm

##21. Merge Two Sorted Lists

~~~
class Solution:
    def mergeTwoLists(self, l1, l2):
        """
        :type l1: ListNode
        :type l2: ListNode
        :rtype: ListNode
        """
        result = ListNode(0);
        curr = result
        while True:
            if l1 and l2:
                if l1.val <= l2.val:
                    curr.next = ListNode(l1.val)
                    l1 = l1.next
                else:
                    curr.next = ListNode(l2.val)
                    l2 = l2.next
                curr = curr.next
            else:
                break
        if l1:
            curr.next = l1
        elif l2:
            curr.next = l2

        return result.next
~~~

#2.Review --[应该多问问题的9个原因](https://medium.com/s/story/9-reasons-to-ask-more-questions-43fb61dbf73f)
    更受欢迎
    被认为更能干
    你将确实更胜任
    提升亲密关系
    成为更具创造力的思考者
    更勇敢
    更有智慧
    成为更好的领导者
    更有趣
#3.Tips
    用普元的EOS作为开发平台，搭建集群时，需要把缓存CacheForUserObject在配置文件中改为CacheMode=REPL_SYNC,IsClustered=true,否则请求在服务器间转移时，有短暂的登陆用户信息查询不到，导致跳转到登陆页面。

#4.Share
    对于浏览器工作原理的解释,视频《像素的一生》来自微博@韦字只念第二声的分享,[油管地址](https://www.youtube.com/watch?v=NCUDntd-3ao&feature=youtu.be)，[B站地址](https://www.bilibili.com/video/av35265997/)