---
title: NDIS Filter Drivers
description: NDIS 6.0 introduced NDIS filter drivers. Filter drivers can monitor and modify the interaction between protocol drivers and miniport drivers.
ms.date: 09/27/2024
---

# Filter drivers

NDIS 6.0 introduced NDIS filter drivers. Filter drivers can monitor and modify the interaction between protocol drivers and miniport drivers. Filter drivers are easier to implement and have less processing overhead than NDIS intermediate drivers.

A *filter module* is an instance of a filter driver. As the following figure illustrates, filter modules are typically layered between miniport adapters and protocol bindings.

:::image type="content" source="images/filter-stack.png" alt-text="Diagram illustrating an NDIS driver stack with filter modules between miniport adapters and protocol bindings.":::

A filter driver communicates with NDIS and other NDIS drivers through the NDIS library. The NDIS library exports a full set of functions (**NdisF*Xxx*** and other **Ndis*Xxx*** functions) that encapsulate all of the operating system functions that a filter driver must call. The filter driver, in turn, must export a set of entry points (*FilterXxx* functions) that NDIS calls for its own purposes, or on behalf of other drivers, to access the filter driver.

> [!NOTE]
> For more information about the NDIS driver stack and a diagram showing the relationship between all four NDIS driver types, see [NDIS Driver Stack](ndis-driver-stack.md).

## Related content

- [Roadmap for Developing NDIS Filter Drivers](./roadmap-for-developing-ndis-filter-drivers.md)
- [Network API reference](/windows-hardware/drivers/ddi/_netvista/)
