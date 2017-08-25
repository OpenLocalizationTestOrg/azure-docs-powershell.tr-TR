---
title: "Azure Stack PowerShell’e genel bakış | Microsoft Docs"
description: "Azure Stack PowerShell yükleme ve yapılandırmasına genel bakış."
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: 2a03697e0f3e80d63c48f2dc5615f6c99b9ef716
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2017
---
# <a name="azure-stack-powershell"></a><span data-ttu-id="04e84-103">Azure Stack PowerShell</span><span class="sxs-lookup"><span data-stu-id="04e84-103">Azure Stack PowerShell</span></span> 

<span data-ttu-id="04e84-104">Azure Stack aşağıdaki iki PowerShell modülünü gerektirir:</span><span class="sxs-lookup"><span data-stu-id="04e84-104">Azure Stack requires the following two PowerShell modules:</span></span>  

1. <span data-ttu-id="04e84-105">**2017-03-09-profile** API Sürüm Profili yüklenerek elde edilen Azure Stack ile uyumlu **AzureRM** modülü.</span><span class="sxs-lookup"><span data-stu-id="04e84-105">The Azure Stack compatible **AzureRM** module which is available by installing the **2017-03-09-profile** API Version Profile.</span></span> <span data-ttu-id="04e84-106">Bu profil kullanılarak yüklenen cmdlet’ler, Azure Stack bulut yöneticileri ve kiracıları tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="04e84-106">The cmdlets installed by using this profile can be used by the Azure Stack cloud administrators and the tenants.</span></span> <span data-ttu-id="04e84-107">Bu profilde mevcut olan PowerShell cmdlet’ler hakkında bilgi almak için [AzureRM modülü 1.2.9 sürümünün](https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-1.2.9) PowerShell başvurusu içeriğine bakın.</span><span class="sxs-lookup"><span data-stu-id="04e84-107">To learn about the PowerShell cmdlets that are available in this profile, see the PowerShell reference content for the [1.2.9 version of AzureRM](https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-1.2.9) module.</span></span>  

2. <span data-ttu-id="04e84-108">**AzureStack** modülünün **1.2.9** sürümü.</span><span class="sxs-lookup"><span data-stu-id="04e84-108">The **1.2.9** version of the **AzureStack** module.</span></span> <span data-ttu-id="04e84-109">Bu modül kullanılarak yüklenen cmdlet’ler yalnızca Azure Stack bulut yöneticileri tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="04e84-109">The cmdlets installed by using this module can be used by Azure Stack cloud administrators only.</span></span> <span data-ttu-id="04e84-110">Yöneticiler teklif, plan, hizmet, fiyat teklifi, vb. yönetme gibi işlemleri bu modülün sağladığı PowerShell cmdlet’lerini kullanarak gerçekleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="04e84-110">Administrator can perform operations such as manage offers, plans, services, quotas, etc. by using the PowerShell cmdlets provided by this module.</span></span> <span data-ttu-id="04e84-111">Bu modülde mevcut olan PowerShell cmdlet’leri hakkında bilgi almak için [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.9#azurerm.azurestackadmin) ve [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.9#azurerm.azurestackstorage) Başvurusu içeriğine bakın.</span><span class="sxs-lookup"><span data-stu-id="04e84-111">To learn about the PowerShell cmdlets available in this module, see the [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.9#azurerm.azurestackadmin) and [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.9#azurerm.azurestackstorage) Reference content.</span></span>

## <a name="next-steps"></a><span data-ttu-id="04e84-112">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="04e84-112">Next Steps</span></span>

* [<span data-ttu-id="04e84-113">Azure Stack için PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="04e84-113">Install PowerShell for Azure Stack</span></span>](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [<span data-ttu-id="04e84-114">PowerShell’i Azure Stack ile kullanmak üzere yapılandırma</span><span class="sxs-lookup"><span data-stu-id="04e84-114">Configure PowerShell for use with Azure Stack</span></span>](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)


