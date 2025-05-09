---
outline: deep
---

# 依赖请求

当请求依赖于另一个请求的结果时，可以使用 [ready](/api-reference/hooks/use-request/request-options.md#ready) 和 [watchSource](/api-reference/hooks/use-request/request-options.md#watchdeep) 方法来实现。

* 当 [ready](/api-reference/hooks/use-request/request-options.md#ready) 为 `false` 时，请求始终不会发出。
* 当 [ready](/api-reference/hooks/use-request/request-options.md#ready) 为 `true` 时，请求具备发送条件，但默认不会立即发出。可通过搭配 [watchSource](/api-reference/hooks/use-request/request-options.md#watchdeep) 实现依赖变化时的自动刷新。

在下面的案例中，数据B依赖于数据A，当数据A为`true`，数据B才会自动发起请求。

::: demo
use-request/dependency-request
https://play.vuejs.org/#eNqtVM1uFDkQfpWi95AZabo7CaCVeiezG1hW2j0sCLjRHDzdlR6TbtvY7pmJRnPgQiQkfi4gxIkDcOPnBgfyNkzEjVeg2s78hEC4cLHscrm+r74q1yTYVioa1hgkQddkmisLBm2toGSi2EoDa9KglwpeKakt2D2FMIGraJQUBi9KYVFYmMKOlhWsCamrkI25NGuLJxOoDV7F2zWanzlmslK1xXzhRrzoPhUZgVlgZk9k2yPGLWz5A7QqXpbcIDnkCYi66qNuw1YPBI7gCsWgu5ZGI8shNmZK7TqvUNZ2bu3ASoh2u0GLY/j84P3s4ZPZnf3Dx+8O77+ZMyjQ/sN28W9m2ZJCO5kjdb/RpesJ9XoN9CQVAMyxXybSOru+vk6gAJpE1wJuUGyMhBy12h2oRY47XGB+MxXTpQ4TyIlA4taNDpSS5VwUyXyzQfJtrYjeWmFNUD6GRpbvkdtc8lbLyXbmjAsaDVlZ48J5FXDzJODmKYAdn7eD6zS7EbPZ4JqsdYbzDCg5gurGvv2o2ehgsVIlSUEngG7Oh25DW9XzJYHtLx+fTSbLpP+Etdm9558PDj59eB1F0RochYfptBurE88vwOHTt7NHr2b7d2cv9mcvD3w4r8sPnhxD3PwRIsmxeN6NPfVuvJIQHY3dKxFMJhXmze8SVASvVJ9lu4WWVPoEhky3wnCowizsF6GRO7b9R+OjWO4LcF6NYYMWZ+1LnaMONbGrTQLnjswV0wUXoebFwCawse7Mrpv6tbVSnIT97Tz+zrDvXmeylDqB0YBbXEGhvyaFN/wSMlT8RhGSIugEfh6EFVPRLSMFTSZHMT26oIGUeNKNbTlJGnMaDKxVJonjWqjdIqL2jpcefzUFMDZGU8Wc/taY4qeBa8sm1KlRjgXIOS3OElVcuChNEEpkSvwt1VXs8OIb9s1X4yXqy8py+lbHsmBlKUf/OZvVNS4oZQPMdr9jv2XGnugVGmOoh7iShiWN0frrS9f+xzHtF5eVzOuSvE+5pCEmy7rh6N0uUFMQ7VWhGrb/umJQ5a+bS2OadmaeVEPUqeH804CG+MVTUl/SPRudW6g4/QolrFlU
:::

