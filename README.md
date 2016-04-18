# Observer
## js观察者模式 订阅发布和退订

### 使用

```
 var blogger = {
        recommend: function (id) {
            var msg = 'dudu 推荐了的帖子:' + id;
            this.publish(msg);
        }
    };
    
    var user = {
        vote: function (id) {
            var msg = '有人投票了!ID=' + id;
            this.publish(msg);
        }
    };
    
    observer.make(blogger);
    observer.make(user);
```

> 观察者的使用场合就是：当一个对象的改变需要同时改变其它对象，并且它不知道具体有多少对象需要改变的时候，就应该考虑使用观察者模式。

> 总的来说，观察者模式所做的工作就是在解耦，让耦合的双方都依赖于抽象，而不是依赖于具体。从而使得各自的变化都不会影响到另一边的变化。
