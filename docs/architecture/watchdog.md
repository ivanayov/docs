## OpenFaaS watchdog

The OpenFaaS watchdog is responsible for starting and monitoring functions in OpenFaaS. Any binary can become a function through use of the watchdog.

## Classic watchdog

The classic watchdog is currently used in all the official OpenFaaS templates. You can view the templates in the [templates repository](https://github.com/openfaas/templates).

<a href="https://camo.githubusercontent.com/61c169ab5cd01346bc3dc7a11edc1d218f0be3b4/68747470733a2f2f7062732e7477696d672e636f6d2f6d656469612f4447536344626c554941416f34482d2e6a70673a6c61726765"><img src="https://camo.githubusercontent.com/61c169ab5cd01346bc3dc7a11edc1d218f0be3b4/68747470733a2f2f7062732e7477696d672e636f6d2f6d656469612f4447536344626c554941416f34482d2e6a70673a6c61726765"></a>

*Pictured: technical conceptual diagram of the OpenFaaS watchdog during an invocation*

Technical documentation on the classic watchdog is available belong along with a table with all configuration options.

* [Watchdog README](https://github.com/openfaas/faas/tree/master/watchdog)

## of-watchdog

of-watchdog is our next-generation watchdog which is in incubation within our [openfaas-incubator organisation](https://github.com/openfaas-incubator).

<a href="/architecture/watchdog-modes.png"><img src="/architecture/watchdog-modes.png"></a>

*Pictured: various modes for the of-watchdog component*

This brings version of the watchdog brings new features for high-throughput systems. The primary difference is the ability to keep a process warm between invocations. The classic watchdog forks one process per request and the new version enables a mode where that same process can be re-used repeatedly to reduce latency.

* [Read more on the of-watchdog](https://github.com/openfaas-incubator/of-watchdog)
