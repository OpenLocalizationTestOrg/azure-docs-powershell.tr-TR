---
title: "Azure PowerShell’e Genel Bakış | Microsoft Docs"
description: "Yükleme ve yapılandırma bağlantılarıyla birlikte Azure PowerShell’e genel bakış."
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 07/26/2017
ms.openlocfilehash: 3772b68949dc9dba110e6015c8d2a8b944b26528
ms.sourcegitcommit: 20bcef86db4e4869125bb63085fcffd009c19280
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/27/2017
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="8947f-103">Azure PowerShell’e Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="8947f-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="8947f-104">Azure PowerShell, Azure kaynaklarınızı yönetmek için [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modelini kullanan bir dizi cmdlet sunar.</span><span class="sxs-lookup"><span data-stu-id="8947f-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span>

<span data-ttu-id="8947f-105">Sisteminizde Azure PowerShell’i çalıştırmaya başlamak için [Yükleme](install-azurerm-ps.md) makalesini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="8947f-105">Review the [Install](install-azurerm-ps.md) article to get Azure PowerShell up and running on your system.</span></span> <span data-ttu-id="8947f-106">Daha sonra, hizmeti kullanmaya başlamak için [Başlangıç](get-started-azureps.md) makalesini okuyun.</span><span class="sxs-lookup"><span data-stu-id="8947f-106">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="8947f-107">En son sürüm hakkında bilgi edinmek için [sürüm notlarına](release-notes-azureps.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="8947f-107">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="8947f-108">Aşağıdaki örnekler, yaygın senaryoları Azure PowerShell ile nasıl gerçekleştireceğinizi öğrenmenize yardımcı olabilir:</span><span class="sxs-lookup"><span data-stu-id="8947f-108">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="8947f-109">Linux Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="8947f-109">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="8947f-110">Windows Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="8947f-110">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="8947f-111">Web Apps</span><span class="sxs-lookup"><span data-stu-id="8947f-111">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="8947f-112">SQL Veritabanları</span><span class="sxs-lookup"><span data-stu-id="8947f-112">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)


> [!NOTE]<span data-ttu-id="8947f-113"> > Dönüştürülemeyen klasik dağıtım modelini kullanan dağıtımlarınız varsa, Azure PowerShell'in Hizmet Yönetimi sürümünü yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8947f-113"> > If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="8947f-114">Daha fazla bilgi için bkz. [Azure PowerShell Hizmet Yönetimi modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="8947f-114">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>


### <a name="need-help-with-powershell"></a><span data-ttu-id="8947f-115">PowerShell konusunda yardıma mı ihtiyacınız var?</span><span class="sxs-lookup"><span data-stu-id="8947f-115">Need help with PowerShell?</span></span>

<span data-ttu-id="8947f-116">PowerShell'i tanımıyorsanız, PowerShell'e giriş makalesi size yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="8947f-116">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span> <span data-ttu-id="8947f-117">PowerShell’i kullanmaya başlamak için bkz. [PowerShell ile Betik Oluşturma](https://technet.microsoft.com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="8947f-117">To get started with PowerShell, see [Scripting with PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span></span>

<span data-ttu-id="8947f-118">Şu videoyu da izleyebilirsiniz: [Temel PowerShell Bilgileri: (1. Bölüm) PowerShell’i Kullanmaya Başlama](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="8947f-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="8947f-119">Diğer Azure PowerShell modülleri</span><span class="sxs-lookup"><span data-stu-id="8947f-119">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="8947f-120">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8947f-120">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="8947f-121">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="8947f-121">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="8947f-122">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8947f-122">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="8947f-123">Azure Elastik DB</span><span class="sxs-lookup"><span data-stu-id="8947f-123">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
