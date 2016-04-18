# Observer
js观察者模式 订阅发布和退订
`var blogger = {
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
observer.make(user);`
