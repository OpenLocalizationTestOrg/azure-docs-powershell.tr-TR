---
title: "Azure PowerShell Değişiklik Günlüğü | Microsoft Docs"
description: "Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 04f89e8d47d0825d46cb1b8817efbcc0cafa0acd
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a><span data-ttu-id="6efbb-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="6efbb-103">Release notes</span></span>

<span data-ttu-id="6efbb-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6efbb-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-380"></a><span data-ttu-id="6efbb-105">Sürüm 3.8.0</span><span class="sxs-lookup"><span data-stu-id="6efbb-105">Version 3.8.0</span></span>
* <span data-ttu-id="6efbb-106">İşlem</span><span class="sxs-lookup"><span data-stu-id="6efbb-106">Compute</span></span>
  - <span data-ttu-id="6efbb-107">Get-* cmdlet’lerinde birden fazla veri sayfasını (120’den fazla öğe) almaya olanak tanıyan hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="6efbb-107">Fix bug in Get-* cmdlets, to allow retrieving multiple pages of data (more than 120 items)</span></span>
* <span data-ttu-id="6efbb-108">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6efbb-108">DataLakeAnalytics</span></span>
  - <span data-ttu-id="6efbb-109">Bazı komutların uygun anlatım ve örnekler içermesine yönelik yardım düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6efbb-109">Fix help for some commands to have the proper verbage and examples.</span></span>
* <span data-ttu-id="6efbb-110">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6efbb-110">DataLakeStore</span></span>
  - <span data-ttu-id="6efbb-111">`Get-AzureRMDataLakeStoreItemContent` cmdlet’i için tam destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="6efbb-111">Add support for head and tail to the `Get-AzureRMDataLakeStoreItemContent` cmdlet.</span></span> <span data-ttu-id="6efbb-112">Bu değişiklik, ilk N veya son N yeni çizgi ile ayrılmış satırın gösterilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="6efbb-112">This enables returning the top N or last N new line delimited rows to be displayed.</span></span>
* <span data-ttu-id="6efbb-113">HDInsight</span><span class="sxs-lookup"><span data-stu-id="6efbb-113">HDInsight</span></span>
  - <span data-ttu-id="6efbb-114">RServer küme türü için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="6efbb-114">Added support for RServer cluster type</span></span>
    + <span data-ttu-id="6efbb-115">New-AzureRmHDInsightCluster veya New-AzureRmHDInsightClusterConfig içindeki RServer kümesi için Edgenode VM boyutu belirtilebilir</span><span class="sxs-lookup"><span data-stu-id="6efbb-115">Edgenode VM size can be specified for RServer cluster in New-AzureRmHDInsightCluster or New-AzureRmHDInsightClusterConfig</span></span>
    + <span data-ttu-id="6efbb-116">RServer artık Add-AzureRmHDInsightConfigValues içinde bir yapılandırma seçeneğidir.</span><span class="sxs-lookup"><span data-stu-id="6efbb-116">RServer is now a configuration option in Add-AzureRmHDInsightConfigValues.</span></span> <span data-ttu-id="6efbb-117">RStudio yüklemesinin yapılması gerektiğini belirtmek üzere R Studio bayrağının ayarlanmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6efbb-117">It allows for RStudio flag to be set to indicate that R Studio installation should be done.</span></span>
* <span data-ttu-id="6efbb-118">LogicApp</span><span class="sxs-lookup"><span data-stu-id="6efbb-118">LogicApp</span></span>
  - <span data-ttu-id="6efbb-119">Set-AzureRmIntegrationAccountSchema ve Set-AzureRmIntegrationAccountMap cmdlet’lerinin contentlink sorunu düzeltilmiştir (Hem content hem de contentlink’in ayarlanması güncelleştirme hatasına neden oluyordu).</span><span class="sxs-lookup"><span data-stu-id="6efbb-119">Set-AzureRmIntegrationAccountSchema and Set-AzureRmIntegrationAccountMap cmdlets are fixed for the contentlink issue(Both content and contentlink were set resulting in update failure).</span></span>
* <span data-ttu-id="6efbb-120">Ağ</span><span class="sxs-lookup"><span data-stu-id="6efbb-120">Network</span></span>
  - <span data-ttu-id="6efbb-121">Application Gateway’lere yeni web uygulaması güvenlik duvarı özellikleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="6efbb-121">Added support for new web application firewall features to Application Gateways</span></span>
    + <span data-ttu-id="6efbb-122">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig eklendi</span><span class="sxs-lookup"><span data-stu-id="6efbb-122">Added New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>
    + <span data-ttu-id="6efbb-123">Get-AzureRmApplicationGatewayAvailableWafRuleSets eklendi (Diğer ad: List-AzureRmApplicationGatewayAvailableWafRuleSets)</span><span class="sxs-lookup"><span data-stu-id="6efbb-123">Added Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)</span></span>
    + <span data-ttu-id="6efbb-124">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration güncelleştirildi: -RuleSetType -RuleSetVersion ve -DisabledRuleGroups parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6efbb-124">Updated New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
    + <span data-ttu-id="6efbb-125">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration güncelleştirildi: -RuleSetType -RuleSetVersion ve -DisabledRuleGroups parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6efbb-125">Updated Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
  - <span data-ttu-id="6efbb-126">Sanal Ağ Geçidi Bağlantılarına IPSec ilkeleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6efbb-126">Added support for IPSec policies to Virtual Network Gateway Connections</span></span>
  - <span data-ttu-id="6efbb-127">New-AzureRmIpsecPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="6efbb-127">Added New-AzureRmIpsecPolicy</span></span>
  - <span data-ttu-id="6efbb-128">New-AzureRmVirtualNetworkGatewayConnection güncelleştirildi: -IpsecPolicies ve -UsePolicyBasedTrafficSelectors parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6efbb-128">Updated New-AzureRmVirtualNetworkGatewayConnection: Added parameter -IpsecPolicies and -UsePolicyBasedTrafficSelectors</span></span>
* <span data-ttu-id="6efbb-129">Profil</span><span class="sxs-lookup"><span data-stu-id="6efbb-129">Profile</span></span>
  - <span data-ttu-id="6efbb-130">*Eski*: Save-AzureRmProfile, Save-AzureRmContext olarak yeniden adlandırıldı, eski cmdlet adının diğer adı var ve diğer sonraki sürümde kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="6efbb-130">*Obsolete*: Save-AzureRmProfile is renamed to Save-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="6efbb-131">*Eski*: Select-AzureRmProfile, Import-AzureRmContext olarak yeniden adlandırıldı, eski cmdlet adının diğer adı var ve diğer sonraki sürümde kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="6efbb-131">*Obsolete*: Select-AzureRmProfile is renamed to Import-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="6efbb-132">Profil cmdlet’lerinin PSAzureContext ve PSAzureProfile çıktı türleri sonraki sürümde değiştirilecek.</span><span class="sxs-lookup"><span data-stu-id="6efbb-132">The PSAzureContext and PSAzureProfile output types of profile cmdlets will be changed in the next release.</span></span>
  - <span data-ttu-id="6efbb-133">Save-AzureRmContext cmdlet’i sonraki sürümde OutputType içermeyecek.</span><span class="sxs-lookup"><span data-stu-id="6efbb-133">The Save-AzureRmContext cmdlet will have no OutputType in the next release.</span></span>
  - <span data-ttu-id="6efbb-134">Cmdlet ortak kodunda veri karmaları için FIPS ile uyumlu algoritma kullanma hatası düzeltildi: https://github.com/Azure/azure-powershell/issues/3651</span><span class="sxs-lookup"><span data-stu-id="6efbb-134">Fix bug in cmdlet common code to use FIPS-compliant algorithm for data hashes: https://github.com/Azure/azure-powershell/issues/3651</span></span>
* <span data-ttu-id="6efbb-135">Sql</span><span class="sxs-lookup"><span data-stu-id="6efbb-135">Sql</span></span>
  - <span data-ttu-id="6efbb-136">Azure Yük Devretme Grubu Cmdlet’lerinde hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="6efbb-136">Bug fixes on Azure Failover Group Cmdlets</span></span>
  - <span data-ttu-id="6efbb-137">İşlem yoklaması için düzeltme</span><span class="sxs-lookup"><span data-stu-id="6efbb-137">Fix for operation polling</span></span>
  - <span data-ttu-id="6efbb-138">FailoverPolicy değeri El ile olarak ayarlanırken GracePeriodWithDataLossHour değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6efbb-138">Fix GracePeriodWithDataLossHour value when setting FailoverPolicy to Manual</span></span>
* <span data-ttu-id="6efbb-139">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6efbb-139">TrafficManager</span></span>
  - <span data-ttu-id="6efbb-140">Coğrafi trafik yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="6efbb-140">Support for the Geographic traffic routing method</span></span>
    + <span data-ttu-id="6efbb-141">New-AzureRmTrafficManagerProfile cmdlet’inin TrafficRoutingMethod parametresi için yeni 'Geographic' değeri</span><span class="sxs-lookup"><span data-stu-id="6efbb-141">New value 'Geographic' for the TrafficRoutingMethod parameter of New-AzureRmTrafficManagerProfile</span></span>
    + <span data-ttu-id="6efbb-142">New-AzureRmTrafficManagerEndpoint ve Add-AzureRmTrafficManagerEndpointConfig için yeni 'GeoMapping' parametresi</span><span class="sxs-lookup"><span data-stu-id="6efbb-142">New parameter 'GeoMapping' for the New-AzureRmTrafficManagerEndpoint and Add-AzureRmTrafficManagerEndpointConfig</span></span>
    + <span data-ttu-id="6efbb-143">Profil koleksiyonu döndürdüğünde Get-AzureRmTrafficManagerProfile kanalları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6efbb-143">Fix piping for Get-AzureRmTrafficManagerProfile when it returns a collection of profiles</span></span>
* <span data-ttu-id="6efbb-144">ServiceManagement</span><span class="sxs-lookup"><span data-stu-id="6efbb-144">ServiceManagement</span></span>
  - <span data-ttu-id="6efbb-145">Restart-AzureVM: VM’yi yeniden başlatma sırasında bakım gerçekleştirmeye yönelik InitiateMaintenance parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6efbb-145">Restart-AzureVM: Added InitiateMaintenance parameter for performing maintenance during VM restart.</span></span>
  - <span data-ttu-id="6efbb-146">Get-AzureVM: Bakım Durumu alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="6efbb-146">Get-AzureVM: Added Maintenance Status field.</span></span>
  - <span data-ttu-id="6efbb-147">Kurtarma Hizmetleri kasası yükseltmesini destekleyen yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="6efbb-147">Added new cmdlets to support Recovery Services vault upgrade</span></span>
    + <span data-ttu-id="6efbb-148">Test-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="6efbb-148">Test-AzureRecoveryServicesVaultUpgrade</span></span>
    + <span data-ttu-id="6efbb-149">Invoke-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="6efbb-149">Invoke-AzureRecoveryServicesVaultUpgrade</span></span>