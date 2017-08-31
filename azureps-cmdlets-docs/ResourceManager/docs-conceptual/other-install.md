---
title: "Azure PowerShell'i yüklemenin diğer yolları | Microsoft Docs"
description: "Azure PowerShell’i MSI paketini veya Web Platformu Yükleyicisi’ni kullanarak yükleme."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 9cee582f74b7f3260c6ae167a8ac358d360ad8ab
ms.sourcegitcommit: 45587b5091293288e16cfae8ac412e0d42f8f450
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2017
---
# <a name="other-installation-methods"></a><span data-ttu-id="291d5-103">Diğer yükleme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="291d5-103">Other installation methods</span></span>

<span data-ttu-id="291d5-104">Azure PowerShell’i yüklemek için birden çok yöntem vardır.</span><span class="sxs-lookup"><span data-stu-id="291d5-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="291d5-105">Tercih edilen yöntem, PowerShell Galerisi ile PowerShellGet’i kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="291d5-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="291d5-106">Azure PowerShell, Web Platformu Yükleyicisi (WebPI) ya da [GitHub](https://github.com/Azure/azure-powershell/releases/latest)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="291d5-106">Azure PowerShell can be installed using the Web Platform Installer (WebPI) or by using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span>

## <a name="docker"></a><span data-ttu-id="291d5-107">Docker</span><span class="sxs-lookup"><span data-stu-id="291d5-107">Docker</span></span>

<span data-ttu-id="291d5-108">Azure PowerShell ile önceden yapılandırılmış bir Docker görüntüsü sunuyoruz.</span><span class="sxs-lookup"><span data-stu-id="291d5-108">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="291d5-109">Kapsayıcıyı `docker run` komutuyla çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="291d5-109">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="291d5-110">Ayrıca, bir PowerShell Core kapsayıcısı olarak bir cmdlet alt kümesi sunarız.</span><span class="sxs-lookup"><span data-stu-id="291d5-110">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="291d5-111">Mac/Linux için `latest` görüntüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="291d5-111">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="291d5-112">Windows için `nanoserver` görüntüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="291d5-112">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="291d5-113">Azure PowerShell, [PowerShell Galerisi](https://www.powershellgallery.com/)’nden `Install-Module` aracılığıyla görüntüye yüklenir.</span><span class="sxs-lookup"><span data-stu-id="291d5-113">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>

## <a name="install-using-the-web-platform-installer"></a><span data-ttu-id="291d5-114">Web platformu yükleyicisini kullanarak yükleme</span><span class="sxs-lookup"><span data-stu-id="291d5-114">Install using the Web Platform Installer</span></span>

<span data-ttu-id="291d5-115">WebPI’dan en son Azure PowerShell’i yükleme işlemi, önceki sürümlerde olduğu gibidir.</span><span class="sxs-lookup"><span data-stu-id="291d5-115">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="291d5-116">[Azure PowerShell WebPI paketini](http://aka.ms/webpi-azps) indirin ve yükleme işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="291d5-116">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="291d5-117">Daha önce PowerShell Galerisi'nden Azure modülleri yüklediyseniz, yükleyici bunları otomatik olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="291d5-117">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="291d5-118">Bu, Azure PowerShell’in yalnızca bir sürümünün yüklü olmasını sağlayarak ortamınızı basitleştirir.</span><span class="sxs-lookup"><span data-stu-id="291d5-118">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="291d5-119">Bununla birlikte, aynı anda birden çok sürümün yüklü olmasını gerektiren senaryolar da vardır.</span><span class="sxs-lookup"><span data-stu-id="291d5-119">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="291d5-120">PowerShell Galerisi modülleri `$env:ProgramFiles\WindowsPowerShell\Modules` konumuna yüklenir.</span><span class="sxs-lookup"><span data-stu-id="291d5-120">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="291d5-121">Buna karşılık, WebPI yükleyicisi Azure modüllerini `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` konumuna yükler.</span><span class="sxs-lookup"><span data-stu-id="291d5-121">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="291d5-122">Yükleme sırasında bir hata oluşursa, `$env:ProgramFiles\WindowsPowerShell\Modules` klasörünüzdeki Azure* klasörlerini el ile kaldırabilir ve yüklemeyi yeniden deneyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="291d5-122">If an error occurs during install, you can manually remove the Azure* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="291d5-123">Yükleme tamamlandığında, `$env:PSModulePath` ayarınız Azure PowerShell cmdlet’lerini içeren dizinleri içermelidir.</span><span class="sxs-lookup"><span data-stu-id="291d5-123">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="291d5-124">Azure PowerShell’in düzgün yüklendiğini doğrulamak için aşağıdaki komut kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="291d5-124">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="291d5-125">PowerShell’i WebPI’dan yüklerken karşılaşabileceğiniz bilinen bir sorun vardır.</span><span class="sxs-lookup"><span data-stu-id="291d5-125">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="291d5-126">Bilgisayarınızın sistem güncelleştirmeleri veya başka yüklemeler nedeniyle yeniden başlatılması gerekiyorsa, `$env:PSModulePath` güncelleştirmeleri Azure PowerShell’in yüklü olduğu yolu içermeyebilir.</span><span class="sxs-lookup"><span data-stu-id="291d5-126">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="291d5-127">Yükleme işleminden sonra cmdlet’leri yüklemeye veya yürütmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="291d5-127">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="291d5-128">Bu hata, makine yeniden başlatılarak ya da tam yol ile modül içeri aktarılarak düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="291d5-128">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="291d5-129">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="291d5-129">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-using-the-msi-package"></a><span data-ttu-id="291d5-130">MSI Paketini kullanarak yükleme</span><span class="sxs-lookup"><span data-stu-id="291d5-130">Install using the MSI Package</span></span>

<span data-ttu-id="291d5-131">Azure PowerShell, [GitHub](https://github.com/Azure/azure-powershell/releases/latest)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="291d5-131">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="291d5-132">Azure modüllerinin önceki sürümlerini yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="291d5-132">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="291d5-133">MSI paketi, modülleri `$env:ProgramFiles\WindowsPowerShell\Modules` konumuna yükler ancak sürüme özel klasörler oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="291d5-133">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>
