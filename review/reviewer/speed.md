# 代码评论速度
## 为什么代码评论要快？
在谷歌，我们优化了开发团队可以共同生产产品的速度，而不是优化单个开发人员编写代码的速度。个人发展的速度很重要，它并不像整个团队的速度那么重要。

当代码审查很慢时，会发生以下几件事：

- 整个团队的速度降低了。是的，没有快速回复评论的个人完成了其他工作。但是，每个CL等待审核和重新审核时，团队其他成员的新功能和错误修复会延迟数天，数周或数月。
- 开发人员开始抗议代码审查流程。如果审阅者每隔几天只响应一次，但每次都要求对CL进行重大更改，那么开发人员可能会感到沮丧和困难。通常，这表达为对评论者的“严格”程度的抱怨。如果审阅者请求相同的实质性更改（确实可以改善代码运行状况的更改），但每次开发人员进行更新时响应都很快，则投诉往往会消失。大多数关于代码审查过程的投诉实际上是通过加快流程来解决的。
- 代码运行状况可能会受到影响。当评论缓慢时，允许开发人员提交不尽如人意的CL的压力越来越大。慢速评论还会阻止代码清理，重构以及对现有CL的进一步改进。

## 代码评审应该有多快？
如果您没有处于重点任务的中间，那么您应该在它进入后不久进行代码审查。

**一个工作日是响应代码审查请求所需的最长时间** （即第二天早上的第一件事）。

遵循这些指导意味着典型的CL应该在一天内进行多轮审查（如果需要）。

## 速度与中断
有一次考虑个人速度胜过团队速度。如果您正处于重点任务的中间，例如编写代码，请不要打断自己进行代码审查。研究表明，开发人员在被打断后可能需要很长时间才能恢复顺畅的开发流程。因此，编写代码时打断自己实际上比让另一位开发人员等待代码审查更加昂贵。

相反，在回复审核请求之前，请等待工作中断点。这可能是当你的当前编码任务完成，午餐后，从会议返回，从微型厨房回来等等。

## 快速回复
当我们谈论代码审查的速度时，我们关注的是响应时间，而不是CL需要多长时间才能完成整个审核并提交。理想情况下，整个过程也应该是快速的，但对于快速到来的个人响应而言，比整个过程快速发生更为重要。

即使有时需要很长时间才能完成整个审核流程，但在整个过程中获得审核者的快速响应可以显着减轻开发人员对“慢速”代码审核感到的挫败感。

如果您太忙而无法对CL进行全面审核，您仍然可以发送快速回复，让开发人员知道您什么时候开始，建议其他能够更快回复的审核人员，或者提供一些初步的广泛评论。 （注意：这并不意味着你应该中断编码，甚至发送这样的响应 - 在工作中的合理断点发送响应。）

重要的是，审核人员要花足够的时间进行审核，确信他们的“LGTM”意味着“此代码符合我们的标准”。但是，理想情况下，个人反应应该很快。

## 跨时区评论
在处理时区差异时，尝试在他们还在办公室时回复作者。如果他们已经回家了，那么请确保在第二天回到办公室之前完成审核。

## LGTM评论
为了加快代码审查，在某些情况下，审阅者应该给予LGTM / Approval，即使他们也在CL上留下未解决的评论。这可以在以下任何一种情

- 审稿人确信开发人员将适当地处理所有审阅者的剩余评论。
- 其余的更改很小，不必由开发人员完成。
如果不清楚的话，审核人应该指定他们想要哪些选项。

当开发人员和审阅者处于不同的时区时，LGTM With Comments尤其值得考虑，否则开发人员将等待一整天才能获得“LGTM，Approval”。

## 大型CL
如果有人向您发送了如此大的代码审查，您不确定何时可以有时间查看它，那么您的典型响应应该是要求开发人员将CL拆分为几个彼此构建的较小的CL而不是一个必须一次审查的巨大的CL。这通常是可能的，对审阅者非常有帮助，即使它需要开发人员的额外工作。

如果CL无法分解为较小的CL，并且您没有时间快速查看整个内容，那么至少要对CL的整体设计写一些评论并将其发送回开发人员以进行改进。作为审阅者，您的目标之一应该是始终取消阻止开发人员或使他们能够快速采取某种进一步的操作，而不会牺牲代码运行状况。

## 代码审查随着时间的推移而改进
如果您遵循这些准则，并且您对代码审查非常严格，那么您应该会发现整个代码审核流程会随着时间的推移而变得越来越快。开发人员可以了解健康代码所需的内容，并向您发送从一开始就很棒的CL，这需要越来越少的审核时间。审阅者学会快速响应，而不是在审核过程中添加不必要的延迟。但是，不要在代码审查标准或质量方面妥协，以实现速度的想象性改进 - 从长远来看，它实际上不会使任何事情发生得更快。

## 紧急情况
还有一些紧急情况，CL必须非常迅速地通过整个审查过程，并且质量准则将放宽。但是，请看什么是紧急情况？描述哪些情况实际上属于紧急情况，哪些情况不符合紧急情况。

下一页：[如何编写代码审查注释]()