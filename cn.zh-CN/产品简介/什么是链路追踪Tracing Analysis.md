# 什么是链路追踪Tracing Analysis

链路追踪Tracing Analysis为分布式应用的开发者提供了完整的调用链路还原、调用请求量统计、链路拓扑、应用依赖分析等工具，可以帮助开发者快速分析和诊断分布式应用架构下的性能瓶颈，提高微服务时代下的开发诊断效率。

## 产品架构

链路追踪的产品架构如下图所示。

![Tracing Analysis Workflow](http://aliware-images.oss-cn-hangzhou.aliyuncs.com/arms/xtrace_dg_workflow.png "链路追踪产品架构")

链路追踪的主要工作流程如下：

1.  客户侧的应用程序通过集成链路追踪的多语言客户端SDK上报服务调用数据。链路追踪支持多种开源社区的SDK，且支持OpenTracing标准。
2.  数据上报至链路追踪控制台后，链路追踪组件进行实时聚合计算和持久化，形成链路明细、性能总览、实时拓扑等监控数据。您可以据此进行问题排查与诊断。
3.  调用链数据可对接下游阿里云产品，例如LogSearch、CloudMonitor、MaxCompute等，用于离线分析、报警等场景。

## 产品功能

链路追踪的主要功能如下：

-   分布式调用链查询和诊断：追踪分布式架构中的所有微服务用户请求，并将它们汇总成分布式调用链。
-   应用性能实时汇总：通过追踪整个应用程序的用户请求，来实时汇总组成应用程序的单个服务和资源。
-   分布式拓扑动态发现：用户的所有分布式微服务应用和相关PaaS产品可以通过链路追踪收集到的分布式调用信息。
-   多语言开发程序接入：基于OpenTracing标准，全面兼容开源社区，例如Jaeger、Zipkin。
-   丰富的下游对接场景：收集的链路可直接用于日志分析，且可对接到MaxCompute等下游分析平台。

