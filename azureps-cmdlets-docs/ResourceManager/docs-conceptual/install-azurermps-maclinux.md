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
ms.sourcegitcommit: 202ec2df66c40a60f47ea06b30a6701ad444d229
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2017
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="b4c71-103">Azure PowerShell'i macOS ve Linux'a yükleme ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b4c71-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="b4c71-104">PowerShell 6 (beta) ve Azure PowerShell uygulamalarını artık Windows dışındaki platformlara yüklemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="b4c71-104">It is now possible to install PowerShell 6 (beta) and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="b4c71-105">Azure PowerShell'i macOS ve Linux'a yükleme adımları Windows ile benzerdir, ancak önce PowerShell 6'yı (beta) yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4c71-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell 6 (beta).</span></span>

> [!NOTE]

> <span data-ttu-id="b4c71-106">PowerShell 6 (beta) ve .NET Core için Azure PowerShell, şu anda beta sürümündedir.</span><span class="sxs-lookup"><span data-stu-id="b4c71-106">At this time, both PowerShell 6 (beta) and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="b4c71-107">Bu ürünler için sınırlı destek sunulur.</span><span class="sxs-lookup"><span data-stu-id="b4c71-107">Support for these products is limited.</span></span> <span data-ttu-id="b4c71-108">Herhangi bir sorunla karşılaşır veya hata bulursanız, lütfen bunları GitHub üzerinden bildirin.</span><span class="sxs-lookup"><span data-stu-id="b4c71-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="b4c71-109">PowerShell 6 (beta) ile ilgili sorunlar</span><span class="sxs-lookup"><span data-stu-id="b4c71-109">Issues for PowerShell 6 (beta)</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="b4c71-110">Azure PowerShell ile ilgili sorunlar</span><span class="sxs-lookup"><span data-stu-id="b4c71-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-6-beta"></a><span data-ttu-id="b4c71-111">1. Adım: PowerShell 6'yı (beta) yükleme</span><span class="sxs-lookup"><span data-stu-id="b4c71-111">Step 1: Install PowerShell 6 (beta)</span></span>

<span data-ttu-id="b4c71-112">PowerShell 6'yı (beta) yükleme adımları, hedef işletim sistemine göre değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4c71-112">The process of installing PowerShell 6 (beta) on varies depending on the target operating system.</span></span>
<span data-ttu-id="b4c71-113">PowerShell 6'yı (beta) Windows'a yüklemek mümkündür, ancak bu makalede macOS ve Linux ele alınır.</span><span class="sxs-lookup"><span data-stu-id="b4c71-113">While it is possible to install PowerShell 6 (beta) on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="b4c71-114">Azure PowerShell'i Windows üzerinde kullanmak isterseniz, Windows'a yönelik [yükleme](./install-azurerm-ps.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="b4c71-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="b4c71-115">**PowerShell 6**'yı (beta) Linux veya macOS'a yüklemek için aşağıdaki adımları gerçekleştirmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="b4c71-115">To install **PowerShell 6** (beta) on Linux or macOS, you need to:</span></span>

1. <span data-ttu-id="b4c71-116">[GitHub](https://github.com/powershell/powershell#get-powershell)'dan işletim sistemi ve sürümüne uygun olan PowerShell’i indirin</span><span class="sxs-lookup"><span data-stu-id="b4c71-116">Get PowerShell for the specific OS and version, from [GitHub](https://github.com/powershell/powershell#get-powershell)</span></span>
2. <span data-ttu-id="b4c71-117">Yükleme talimatlarını izleyin</span><span class="sxs-lookup"><span data-stu-id="b4c71-117">Follow the installation instructions</span></span>
   - [<span data-ttu-id="b4c71-118">Linux</span><span class="sxs-lookup"><span data-stu-id="b4c71-118">Linux</span></span>](https://github.com/PowerShell/PowerShell/blob/master/docs/installation/linux.md)
   - [<span data-ttu-id="b4c71-119">macOS</span><span class="sxs-lookup"><span data-stu-id="b4c71-119">macOS</span></span>](https://github.com/PowerShell/PowerShell/blob/master/docs/installation/linux.md#macos-1012)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="b4c71-120">2. Adım: .NET Core için Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="b4c71-120">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="b4c71-121">PowerShell 6 (beta), PowerShellGet modülü önceden yüklü biçimde gelir.</span><span class="sxs-lookup"><span data-stu-id="b4c71-121">PowerShell 6 (beta) comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="b4c71-122">Bu sayede PowerShell Galerisi'nde yayımlanmış olan modüller kolayca yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="b4c71-122">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="b4c71-123">Azure PowerShell'i yüklemek için yeni bir PowerShell oturumu açın ve aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="b4c71-123">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="b4c71-124">3. Adım: AzureRM.Netcore modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="b4c71-124">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="b4c71-125">Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4c71-125">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="b4c71-126">Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:</span><span class="sxs-lookup"><span data-stu-id="b4c71-126">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
```

<span data-ttu-id="b4c71-127">İçeri aktarma işlemi tamamlandıktan sonra, aşağıdaki komutla Azure oturumu açmayı deneyerek yeni yüklediğiniz modülü test edebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b4c71-127">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="b4c71-128">Yukarıdaki komut, `https://aka.ms/devicelogin` adresine gidip verilen kodu girmenizi isteyecektir.</span><span class="sxs-lookup"><span data-stu-id="b4c71-128">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="b4c71-129">Kullanılabilen cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="b4c71-129">Available cmdlets</span></span>

<span data-ttu-id="b4c71-130">.NET Standard için Azure PowerShell modülleri geliştirme aşamasındadır.</span><span class="sxs-lookup"><span data-stu-id="b4c71-130">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="b4c71-131">Bu modüller, Windows sürümünde kullanılabilecek tüm cmdlet'leri sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="b4c71-131">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="b4c71-132">AzureRM.Netcore modüllerine aşağıdaki işlevler uygulanmıştır:</span><span class="sxs-lookup"><span data-stu-id="b4c71-132">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="b4c71-133">Hesap yönetimi</span><span class="sxs-lookup"><span data-stu-id="b4c71-133">Account management</span></span>
  - <span data-ttu-id="b4c71-134">Microsoft hesabı, Kuruluş hesabı veya Microsoft Azure Active Directory aracılığıyla Hizmet Sorumlusu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="b4c71-134">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="b4c71-135">Kimlik Bilgilerini Save-AzureRmContext ile diske kaydetme ve kaydedilen kimlik bilgilerini Import-AzureRmContext ile yükleme</span><span class="sxs-lookup"><span data-stu-id="b4c71-135">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="b4c71-136">Ortam</span><span class="sxs-lookup"><span data-stu-id="b4c71-136">Environment</span></span>
  - <span data-ttu-id="b4c71-137">Farklı Microsoft Azure ilk çalıştırma ortamlarına ulaşma</span><span class="sxs-lookup"><span data-stu-id="b4c71-137">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="b4c71-138">Özelleştirilmiş ortamları (Azure Stack veya Windows Azure Paketi ortamlarınız gibi) Ekleme/Ayarlama/Kaldırma</span><span class="sxs-lookup"><span data-stu-id="b4c71-138">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="b4c71-139">Azure hizmetleri için Resource Manager ve Hizmet Yönetim arabirimlerini kullanan yönetim düzlemi cmdlet'leri.</span><span class="sxs-lookup"><span data-stu-id="b4c71-139">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="b4c71-140">Sanal Makine</span><span class="sxs-lookup"><span data-stu-id="b4c71-140">Virtual Machine</span></span>
  - <span data-ttu-id="b4c71-141">App Service (Web siteleri)</span><span class="sxs-lookup"><span data-stu-id="b4c71-141">App Service (Websites)</span></span>
  - <span data-ttu-id="b4c71-142">SQL Database</span><span class="sxs-lookup"><span data-stu-id="b4c71-142">SQL Database</span></span>
  - <span data-ttu-id="b4c71-143">Depolama</span><span class="sxs-lookup"><span data-stu-id="b4c71-143">Storage</span></span>
  - <span data-ttu-id="b4c71-144">Ağ</span><span class="sxs-lookup"><span data-stu-id="b4c71-144">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="b4c71-145">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="b4c71-145">Next Steps</span></span>

<span data-ttu-id="b4c71-146">Azure PowerShell'i kullanma hakkında daha fazla bilgi için [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="b4c71-146">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
