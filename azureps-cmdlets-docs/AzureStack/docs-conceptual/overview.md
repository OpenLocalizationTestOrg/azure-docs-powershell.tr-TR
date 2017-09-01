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
# <a name="azure-stack-powershell"></a>Azure Stack PowerShell 

Azure Stack aşağıdaki iki PowerShell modülünü gerektirir:  

1. **2017-03-09-profile** API Sürüm Profili yüklenerek elde edilen Azure Stack ile uyumlu **AzureRM** modülü. Bu profil kullanılarak yüklenen cmdlet’ler, Azure Stack bulut yöneticileri ve kiracıları tarafından kullanılabilir. Bu profilde mevcut olan PowerShell cmdlet’ler hakkında bilgi almak için [AzureRM modülü 1.2.9 sürümünün](https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-1.2.9) PowerShell başvurusu içeriğine bakın.  

2. **AzureStack** modülünün **1.2.9** sürümü. Bu modül kullanılarak yüklenen cmdlet’ler yalnızca Azure Stack bulut yöneticileri tarafından kullanılabilir. Yöneticiler teklif, plan, hizmet, fiyat teklifi, vb. yönetme gibi işlemleri bu modülün sağladığı PowerShell cmdlet’lerini kullanarak gerçekleştirebilir. Bu modülde mevcut olan PowerShell cmdlet’leri hakkında bilgi almak için [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.9#azurerm.azurestackadmin) ve [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.9#azurerm.azurestackstorage) Başvurusu içeriğine bakın.

## <a name="next-steps"></a>Sonraki Adımlar

* [Azure Stack için PowerShell yükleme](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [PowerShell’i Azure Stack ile kullanmak üzere yapılandırma](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)

