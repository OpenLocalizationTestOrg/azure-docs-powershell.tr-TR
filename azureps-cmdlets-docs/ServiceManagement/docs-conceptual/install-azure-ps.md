---
title: "<span data-ttu-id=\"3f82e-101\">Azure PowerShell Service Management modülünü yükleme ve yapılandırma | Microsoft Docs</span><span class=\"sxs-lookup\"><span data-stu-id=\"3f82e-101\">Install and configure the Azure PowerShell Service Management module | Microsoft Docs</span></span>"
description: "<span data-ttu-id=\"3f82e-102\">Azure PowerShell’i ilk kez kullanmak üzere yükleme ve yapılandırma.</span><span class=\"sxs-lookup\"><span data-stu-id=\"3f82e-102\">How to install and configure Azure PowerShell for first time use.</span></span>"
services: azure
author: sdwheeler
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: c51c727c1cb022eca59f819c7f24d8e058c677da
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="3f82e-103">Azure PowerShell Service Management modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="3f82e-103">Installing the Azure PowerShell Service Management module</span></span>
<a id="installing-the-azure-powershell-service-management-module" class="xliff"></a>

<span data-ttu-id="3f82e-104">Azure PowerShell’in [PowerShell Galerisi](https://www.powershellgallery.com/)’nden yüklenmesi, tercih edilen yükleme yöntemidir.</span><span class="sxs-lookup"><span data-stu-id="3f82e-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <span data-ttu-id="3f82e-105">1. Adım: PowerShellGet yükleme</span><span class="sxs-lookup"><span data-stu-id="3f82e-105">Step 1: Install PowerShellGet</span></span>
<a id="step-1-install-powershellget" class="xliff"></a>

<span data-ttu-id="3f82e-106">PowerShell Galerisi’nden yükleme yapabilmek için PowerShellGet modülü gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f82e-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="3f82e-107">Uygun PowerShellGet sürümüne ve diğer sistem gereksinimlerine sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="3f82e-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="3f82e-108">PowerShellGet’in sisteminizde yüklü olup olmadığını görmek için aşağıdaki komutu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="3f82e-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="3f82e-109">Aşağıdaki çıktıya benzer bir sonuç görmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="3f82e-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="3f82e-110">PowerShellGet yüklü değilse bkz. [PowerShellGet’i edinme](install-azurerm-ps.md#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="3f82e-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](install-azurerm-ps.md#how-to-get-powershellget).</span></span>

## <span data-ttu-id="3f82e-111">2. Adım: Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="3f82e-111">Step 2: Install Azure PowerShell</span></span>
<a id="step-2-install-azure-powershell" class="xliff"></a>

<span data-ttu-id="3f82e-112">Yönetici olarak çalıştırılan Windows PowerShell konsolundan aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="3f82e-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="3f82e-113">Azure modülü, Azure Resource Manager cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="3f82e-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="3f82e-114">AzureRM modülünü yüklediğinizde, daha önce yüklenmemiş diğer Azure modülleri PowerShell Galerisi’nden indirilip yüklenir.</span><span class="sxs-lookup"><span data-stu-id="3f82e-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="3f82e-115">Azure Service Management modülünün, Azure PowerShell Resource Manager modülleriyle ortak bağımlılıkları vardır.</span><span class="sxs-lookup"><span data-stu-id="3f82e-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="3f82e-116">Azure PowerShell Resource Manager modüllerini yüklediyseniz, yükleme komutuna `-AllowClobber` parametresini eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f82e-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="3f82e-117">Bu, mevcut paylaşılan bağımlılıkların güncelleştirilmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3f82e-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="3f82e-118">Bu parametre kullanılmazsa modül yüklenemez.</span><span class="sxs-lookup"><span data-stu-id="3f82e-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="3f82e-119">Bu modülü yükledikten sonra aşağıdaki komutu çalıştırarak modülü içeri aktarabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="3f82e-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <span data-ttu-id="3f82e-120">Cmdlet'leri kullanmak için</span><span class="sxs-lookup"><span data-stu-id="3f82e-120">To use the cmdlets</span></span>
<a id="to-use-the-cmdlets" class="xliff"></a>

<span data-ttu-id="3f82e-121">Azure Service Management cmdlet’leriyle çalışmaya başlamak için öncelikle Azure hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="3f82e-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="3f82e-122">Hesabınızda oturum açmak için aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="3f82e-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="3f82e-123">Azure’da oturum açıldıktan sonra, Azure PowerShell ilgili oturum için bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3f82e-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="3f82e-124">Bu bağlam, ilgili oturum içindeki tüm cmdlet’ler için kullanılacak Azure PowerShell ortamını, hesabını, kiracısını ve aboneliğini içerir.</span><span class="sxs-lookup"><span data-stu-id="3f82e-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="3f82e-125">Artık aşağıdaki modülleri kullanmaya hazırsınız.</span><span class="sxs-lookup"><span data-stu-id="3f82e-125">Now you are ready to use the modules below.</span></span>

## <span data-ttu-id="3f82e-126">Azure Service Management cmdlet’leri</span><span class="sxs-lookup"><span data-stu-id="3f82e-126">Azure Service Management cmdlets</span></span>
<a id="azure-service-management-cmdlets" class="xliff"></a>

<span data-ttu-id="3f82e-127">Azure PowerShell modülleri sık sık güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3f82e-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="3f82e-128">Çevrimiçi cmdlet yardımının modülünüzde olmayan cmdlet’leri veya parametreleri içerdiğini fark ederseniz, modülün en son sürümünü indirip yükleyin.</span><span class="sxs-lookup"><span data-stu-id="3f82e-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="3f82e-129">Modülünüzün sürümün öğrenmek için şunu yazın: `(Get-Module Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="3f82e-129">To find the version of your module, type: `(Get-Module Azure).Version`.</span></span>

<span data-ttu-id="3f82e-130">Azure’daki bazı genel görevleri otomatikleştirmenize yardımcı olabilecek örnek betikler için bkz. [Windows Azure Betik Merkezi](http://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="3f82e-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="3f82e-131">Windows PowerShell’i yükleme, öğrenme, kullanma ve özelleştirme hakkında genel bilgiler için bkz. [Windows PowerShell ile Betik Oluşturma](http://go.microsoft.com/fwlink/p/?linkid=320210).</span><span class="sxs-lookup"><span data-stu-id="3f82e-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>
