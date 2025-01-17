---
title: Feature Flags
aliases: [feature_flags]
cSpell:ignore: OLJCESPC7Z
---

This demo comes with several feature flags which can control failure conditions
in specific services. By default the flags are disabled. Using the Feature Flags
UI <http://localhost:8080/feature> you will be able to control the status of
these feature flags.

| Feature Flag            | Service(s)      | Description                                                                                              |
| ----------------------- | --------------- | -------------------------------------------------------------------------------------------------------- |
| `adServiceFailure`      | Ad Service      | Generate an error for `GetAds` 1/10th of the time                                                        |
| `cartServiceFailure`    | Cart Service    | Generate an error for `EmptyCart` 1/10th of the time                                                     |
| `productCatalogFailure` | Product Catalog | Generate an error for `GetProduct` requests with product id: `OLJCESPC7Z`                                |
| `ItemNotFound`          | Product Catalog | Generate a NotFound error for `GetProduct` requests.                                                     |
| `ItemListInternal`      | Product Catalog | Generate a Internal error for `ListProduct` requests.                                                    |
| `recommendationCache`   | Recommendation  | Create a memory leak due to an exponentially growing cache. 1.4x growth, 50% of requests trigger growth. |
