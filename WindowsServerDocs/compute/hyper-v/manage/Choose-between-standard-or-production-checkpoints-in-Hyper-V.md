---
title: Choose between standard or production checkpoints in Hyper-V
ms.custom: na
ms.prod: windows-server-threshold
ms.reviewer: na
ms.suite: na
ms.technology: 
  - hyper-v
  - techgroup-compute
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 92bb573b-03b7-470e-b72e-e35edf52b349
author: KBDAzure
---
# Choose between standard or production checkpoints in Hyper-V
**This is preliminary content and subject to change.**  
  
Starting with [!INCLUDE[winthreshold_server_1](../../../includes/winthreshold_server_1_md.md)] and [!INCLUDE[winthreshold_client_1](../../../includes/winthreshold_client_1_md.md)], you can choose between standard and production checkpoints for each virtual machine.  
  
Production checkpoints are “point in time” images of a virtual machine, which can be restored later on in a way that is completely supported for all production workloads. This is achieved by using backup technology inside the guest to create the checkpoint, instead of using saved state technology.  
  
Standard checkpoints capture the state, data, and hardware configuration of a running virtual machine and are intended for use in development and test scenarios. Standard checkpoints can be very useful if you need to recreate a specific state or condition of a running virtual machine so that you can troubleshoot a problem.  
  
Production checkpoints are the default for new virtual machines, starting in [!INCLUDE[winthreshold_server_2](../../../includes/winthreshold_server_2_md.md)] and [!INCLUDE[winthreshold_client_2](../../../includes/winthreshold_client_2_md.md)].  
  
## Change checkpoints to production or standard checkpoints  
  
1.  In **Hyper\-V Manager**, right\-click the virtual machine and click **Settings**.  
  
2.  Under the **Management** section, select **Checkpoints**.  
  
3.  Select either production checkpoints or standard checkpoints.  
  
    If you choose production checkpoints, you can also specify whether the host should take a standard checkpoint if a production checkpoint can't be taken. If you clear this checkbox and a production checkpoint cannot be taken, then no checkpoint will be taken.  
  
4.  If you want to store the checkpoint configuration files in a different place, change it in the **Checkpoint File Location** section.  
  
5.  Click **Apply** to apply your changes. If you are done, click **OK** to close the dialog box.  
  
## See also  
  
-   [Production checkpoints](../What-s-new-in-Hyper-V-on-Windows-Server-2016-Technical-Preview.md#BKMK_check)  
  
-   [Enable or disable checkpoints](Enable-or-disable-checkpoints-in-Hyper-V.md)  
  
