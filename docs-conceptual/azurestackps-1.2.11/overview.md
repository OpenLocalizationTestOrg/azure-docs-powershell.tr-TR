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
ms.openlocfilehash: 49980b361c580a1a00f07c2002241e71f2c0b654
ms.sourcegitcommit: df44d5d9874b55455ec745f1846e06a4b3266d13
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2017
---
# <a name="azure-stack-powershell"></a>Azure Stack PowerShell

Azure Stack aşağıdaki iki PowerShell modülünü gerektirir:  

1. **2017-03-09-profile** API Sürüm Profili yüklenerek elde edilen Azure Stack ile uyumlu **AzureRM** modülü. Bu profil kullanılarak yüklenen cmdlet’ler yalnızca Azure Stack operatörleri ve kullanıcıları tarafından kullanılabilir.

2. En güncel sürüm **AzureStack** modülünün **1.2.11** kurulumudur. Bu modül kullanılarak yüklenen cmdlet’ler yalnızca Azure Stack operatörleri tarafından kullanılabilir. Operatörler teklif, plan, hizmet, fiyat teklifi, vb. yönetme gibi işlemleri bu modülün sağladığı PowerShell cmdlet’lerini kullanarak gerçekleştirebilir. Bu modülde mevcut olan PowerShell cmdlet’leri hakkında bilgi almak için [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) ve [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) Başvurusu içeriğine bakın.

## <a name="next-steps"></a>Sonraki Adımlar

* [Azure Stack için PowerShell yükleme](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [PowerShell’i Azure Stack ile kullanmak üzere yapılandırma](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
