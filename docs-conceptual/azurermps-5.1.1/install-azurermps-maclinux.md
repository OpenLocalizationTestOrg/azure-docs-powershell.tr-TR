---
title: "Azure PowerShell'i macOS ve Linux'ta yükleme ve yapılandırma | Microsoft Docs"
description: "Azure PowerShell'i macOS ve Linux'ta yükleme ve ilk kez kullanmak üzere yapılandırma."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 94b39c18acaca7a4b17b5207feed025442665acc
ms.sourcegitcommit: c42c7176276ec4e1cc3360a93e6b15d32083bf9f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2017
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>Azure PowerShell'i macOS ve Linux'a yükleme ve yapılandırma

PowerShell 6 (beta) ve Azure PowerShell uygulamalarını artık Windows dışındaki platformlara yüklemek mümkündür.
Azure PowerShell'i macOS ve Linux'a yükleme adımları Windows ile benzerdir, ancak önce PowerShell 6'yı (beta) yüklemeniz gerekir.

> [!NOTE]

> PowerShell 6 (beta) ve .NET Core için Azure PowerShell, şu anda beta sürümündedir.
> Bu ürünler için sınırlı destek sunulur. Herhangi bir sorunla karşılaşır veya hata bulursanız, lütfen bunları GitHub üzerinden bildirin.
>
> * [PowerShell 6 (beta) ile ilgili sorunlar](https://github.com/PowerShell/PowerShell/issues)
> * [Azure PowerShell ile ilgili sorunlar](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-6-beta"></a>1. Adım: PowerShell 6'yı (beta) yükleme

PowerShell 6'yı (beta) yükleme adımları, hedef işletim sistemine göre değişiklik gösterir.
PowerShell 6'yı (beta) Windows'a yüklemek mümkündür, ancak bu makalede macOS ve Linux ele alınır. Azure PowerShell'i Windows üzerinde kullanmak isterseniz, Windows'a yönelik [yükleme](./install-azurerm-ps.md) makalesine bakın.

**PowerShell 6**'yı (beta) Linux veya macOS'a yüklemek için aşağıdaki adımları gerçekleştirmeniz gerekir:

1. [GitHub](https://github.com/powershell/powershell#get-powershell)'dan işletim sistemi ve sürümüne uygun olan PowerShell’i indirin
2. Yükleme talimatlarını izleyin
   - [Linux](https://github.com/PowerShell/PowerShell/blob/master/docs/installation/linux.md)
   - [macOS](https://github.com/PowerShell/PowerShell/blob/master/docs/installation/linux.md#macos-1012)

## <a name="step-2-install-azure-powershell-for-net-core"></a>2. Adım: .NET Core için Azure PowerShell'i yükleme

PowerShell 6 (beta), PowerShellGet modülü önceden yüklü biçimde gelir. Bu sayede PowerShell Galerisi'nde yayımlanmış olan modüller kolayca yüklenebilir. Azure PowerShell'i yüklemek için yeni bir PowerShell oturumu açın ve aşağıdaki komutu çalıştırın:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>3. Adım: AzureRM.Netcore modülünü yükleme

Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir. Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:

```powershell
Import-Module AzureRM.Netcore
```

İçeri aktarma işlemi tamamlandıktan sonra, aşağıdaki komutla Azure oturumu açmayı deneyerek yeni yüklediğiniz modülü test edebilirsiniz:

```powershell
Login-AzureRMAccount
```

Yukarıdaki komut, `https://aka.ms/devicelogin` adresine gidip verilen kodu girmenizi isteyecektir.

## <a name="available-cmdlets"></a>Kullanılabilen cmdlet'ler

.NET Standard için Azure PowerShell modülleri geliştirme aşamasındadır. Bu modüller, Windows sürümünde kullanılabilecek tüm cmdlet'leri sağlamaz. AzureRM.Netcore modüllerine aşağıdaki işlevler uygulanmıştır:

* Hesap yönetimi
  - Microsoft hesabı, Kuruluş hesabı veya Microsoft Azure Active Directory aracılığıyla Hizmet Sorumlusu ile oturum açma
  - Kimlik Bilgilerini Save-AzureRmContext ile diske kaydetme ve kaydedilen kimlik bilgilerini Import-AzureRmContext ile yükleme
* Ortam
  - Farklı Microsoft Azure ilk çalıştırma ortamlarına ulaşma
  - Özelleştirilmiş ortamları (Azure Stack veya Windows Azure Paketi ortamlarınız gibi) Ekleme/Ayarlama/Kaldırma
* Azure hizmetleri için Resource Manager ve Hizmet Yönetim arabirimlerini kullanan yönetim düzlemi cmdlet'leri.
  - Sanal Makine
  - App Service (Web siteleri)
  - SQL Veritabanı
  - Depolama
  - Ağ

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell'i kullanma hakkında daha fazla bilgi için [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) makalesine bakın.
