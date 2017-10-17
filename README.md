# mit-6.824
MIT 6.824课程的作业，目前完成了raft的所有测试，我用脚本跑过几百次，没有发现问题，如有未发现的错误请指出。最初的raft-v1版本的代码实现思路有部分参考 https://github.com/yuyang0/mit-6.824.git ，当然具体实现亦大有不同。   ~~当前的实现颇为粗糙，没有考虑data race，此外代码结构也不甚清晰，有时间再优化为一个状态机版本，那样实现逻辑会更加清晰。~~ raft-v1这个tag的实现比较粗糙，没有解决data race，代码冗余较多。新写了一个raft-v2版本，解决了data race并优化了部分代码，集中在一个goroutine里面处理raft节点的状态变化，节点状态变化集中处理这部分有参考 https://github.com/happyer/distributed-computing/blob/master/src/raft/raft.go 。测试请使用 go test -race命令，要测试个几百次，如果次数太少了可能有些BUG可能很难测试出来。
- 课程的基本框架代码来自 [git://g.csail.mit.edu/6.824-golabs-2017](git://g.csail.mit.edu/6.824-golabs-2017)
- 课程的实验主页: [https://pdos.csail.mit.edu/6.824/labs/lab-raft.html](https://pdos.csail.mit.edu/6.824/labs/lab-raft.html)
- 课程的一个指导页面： [https://thesquareplanet.com/blog/students-guide-to-raft/](https://thesquareplanet.com/blog/students-guide-to-raft/)
- raft协议论文： [https://pdos.csail.mit.edu/6.824/papers/raft-extended.pdf](https://pdos.csail.mit.edu/6.824/papers/raft-extended.pdf)
- raft的一个简单易懂的动画: [http://thesecretlivesofdata.com/raft/](http://thesecretlivesofdata.com/raft/)
- raft的一个js的实现：[https://github.com/ongardie/raftscope/blob/master/raft.js](https://github.com/ongardie/raftscope/blob/master/raft.js)
