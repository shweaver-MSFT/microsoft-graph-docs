---
title: "Using scoped components in the Microsoft Graph Toolkit"
description: "Use scoped components to prevent name collisions"
localization_priority: Normal
author: shweaver
---

# Using scoped components in the Microsoft Graph Toolkit

Use scoped components to prevent name collisions.

Typically components can be loaded all together with the mgt-loader, or individually referenced with an import statement:
```
import "@microsoft/mgt/dist/es6/components/mgt-person"
```

However, when running in certain environments, such as SharePoint, registering multiple instances of the same component can cause errors in the element registry.

To avoid causing name collisions in the element registry, a *scoped* version of each component can be referenced directly by adding `/scoped` to the end:
```
import "@microsoft/mgt/dist/es6/components/mgt-person/scoped"
```

Using scoped components will scope element tag names avoiding naming collision and allowing multiple versions of the same web component to exist on the page.
