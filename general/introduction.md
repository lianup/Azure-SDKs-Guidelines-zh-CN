# 一般准则: 介绍

The general guidelines are for the benefit of:

一般准则有利于：

- Language-specific guidelines authors.
- Client library designers for languages that have no specific language guidelines.
If you are working in a language with no specific language guidelines, please work with the Azure Developer Experience Architecture Board more closely to ensure the client library is appropriately designed and the developer experience is exemplary.

- 特定语言准则作者。
- 没有特定语言准则的语言的客户端库设计者。
如果您使用的语言没有特定的语言准则，请更密切地与 Azure 开发者体验架构委员会合作，以确保客户端库设计得当，开发者体验优异。

## Design principles

## 设计原则

The Azure SDK should be designed to enhance the productivity of developers connecting to Azure services. Other qualities (such as completeness, extensibility, and performance) are important but secondary. Productivity is achieved by adhering to the principles described below:

Azure SDK 的设计应该提高使用 Azure 服务开发者的生产力。 其他质量（例如完整性、可扩展性、性能）虽然重要，但是是次要的。生产力是通过遵循以下原则实现的：


### Idiomatic

### 符合语言特性

- The SDK should follow the general design guidelines and conventions for the target language. It should feel natural to a developer in the target language.
- We embrace the ecosystem with its strengths and its flaws.
- We work with the ecosystem to improve it for all developers.

- SDK 应该遵循目标语言的一般设计准则和语言习惯。它应该让目标语言开发者感到自然。
- 我们拥抱生态系统的优缺点。
- 我们和生态系统一起为所有开发者改进它。

### Consistent

### 一致性

- Client libraries should be consistent within the language, consistent with the service and consistent between all target languages. In cases of conflict, consistency within the language is the highest priority and consistency between all target languages is the lowest priority.

- 客户端库应该在语言内保持一致，与服务保持一致，并且在所有目标语言间保持一致。在冲突的情况下，在语言内保持一致是最高优先级，在所有目标语言间保持一致是最低优先级。

- Service-agnostic concepts such as logging, HTTP communication, and error handling should be consistent. The developer should not have to relearn service-agnostic concepts as they move between client libraries.

- 日志打印、HTTP 通信、错误处理等与服务无关的概念应该是保持一致的。开发者在不同客户端间迁移时，不应该要重新学习与服务无关的概念。

- Consistency of terminology between the client library and the service is a good thing that aids in diagnosability.

- 在客户端库和服务之间的术语一致性有助于诊断。

- All differences between the service and client library must have a good (articulated) reason for existing, rooted in idiomatic usage rather than whim.

-  在服务和客户端间的所有不一致必须要有一个好的（清晰的）理由，根源在于习惯用法而不是一时兴起。

- The Azure SDK for each target language feels like a single product developed by a single team.

- 每一种目标语言的 Azure SDK 感觉像单个团队开发的单个产品。

There should be feature parity across target languages. This is more important than feature parity with the service.

- 不同目标语言的 SDK 应该有对等功能。这比不同服务间的对等功能更重要。


### Approachable

### 容易上手

- We are experts in the supported technologies so our customers, the developers, don’t have to be.

- 我们是支持技术方面的专家，因此我们的客户和开发者不必如此。

- Developers should find great documentation (hero tutorial, how to articles, samples, and API documentation) that makes it easy to be successful with the Azure service.

- 开发者应该找到优秀的文档（、如何写作、示例和 API 文档） Azure 服务一起取得成功。？

- Getting off the ground should be easy through the use of predictable defaults that implement best practices. Think about progressive concept disclosure.
The SDK should be easily acquired through the most normal mechanisms in the target language and ecosystem.
Developers can be overwhelmed when learning new service concepts. The core use cases should be discoverable.
Diagnosable
The developer should be able to understand what is going on.
It should be discoverable when and under what circumstances a network call is made.
Defaults are discoverable and their intent is clear.
Logging, tracing, and exception handling are fundamental and should be thoughtful.
Error messages should be concise, correlated with the service, actionable, and human readable. Ideally, the error message should lead the consumer to a useful action that they can take.
Integrating with the preferred debugger for the target language should be easy.
Dependable
Breaking changes are more harmful to a user’s experience than most new features and improvements are beneficial.
Incompatibilities should never be introduced deliberately without thorough review and very strong justification.
Do not rely on dependencies that can force our hand on compatibility.