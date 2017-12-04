---
title: about
date: 2017-12-02 13:30:05
type: "about"
---
![码农](/images/IT.gif "This is IT")
# Yittang
**半路出家的野路子，迈向前端攻城狮的方向，也许累，但不悔。**
```
class about {
    constructor(name, Email, QQ) {
        this.name = name;
        this.Email = Email;
        this.QQ = QQ;
    }

    description() {
        return '你好,我叫' + this.name + " ,很高兴来看我的博客！"; 
    }

    myEmail() {
        return '我的Email是：' + this.Email;
    }

    myQQ() {
        return '我的QQ联系方式：' + this.QQ;
    }
}

let id = new about("Yittang", "wjm13262819710@gmail.com", 657217449);
```
