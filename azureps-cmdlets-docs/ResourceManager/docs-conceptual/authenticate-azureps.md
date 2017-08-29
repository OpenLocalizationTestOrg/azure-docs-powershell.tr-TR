---
title: "Azure PowerShell ile oturum açma"
description: "Azure PowerShell ile oturum açma"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: f6d249ca5bb09c4fe8445ba5b339ffa6012815ed
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2017
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="c50ee-103">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="c50ee-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="c50ee-104">Azure PowerShell, birden fazla oturum açma yöntemini destekler.</span><span class="sxs-lookup"><span data-stu-id="c50ee-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="c50ee-105">Hizmeti kullanmaya başlamanın en basit yolu, komut satırından etkileşimli olarak oturum açmaktır.</span><span class="sxs-lookup"><span data-stu-id="c50ee-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="c50ee-106">Etkileşimli oturum açma</span><span class="sxs-lookup"><span data-stu-id="c50ee-106">Interactive log in</span></span>

1. <span data-ttu-id="c50ee-107">`Login-AzureRmAccount` yazın.</span><span class="sxs-lookup"><span data-stu-id="c50ee-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="c50ee-108">Azure kimlik bilgilerinizi isteyen bir iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="c50ee-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="c50ee-109">Hesabınızla ilişkili e-posta adresini ve parolayı yazın.</span><span class="sxs-lookup"><span data-stu-id="c50ee-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="c50ee-110">Azure, kimlik bilgilerini doğrulayıp kaydeder ve pencereyi kapatır.</span><span class="sxs-lookup"><span data-stu-id="c50ee-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="c50ee-111">Hizmet sorumlusu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="c50ee-111">Log in with a service principal</span></span>

<span data-ttu-id="c50ee-112">Hizmet sorumluları kaynakları düzenlemek amacıyla kullanabileceğiniz, etkileşimli olmayan hesaplar oluşturmanız için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="c50ee-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="c50ee-113">Hizmet sorumluları, Azure Active Directory’yi kullanarak kurallarınızı uygulayabileceğiniz kullanıcı hesapları gibidir.</span><span class="sxs-lookup"><span data-stu-id="c50ee-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="c50ee-114">Bir hizmet sorumlusuna gerekli en düşük izinleri vererek otomasyon betiklerinizin daha da güvenli olmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c50ee-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="c50ee-115">Zaten bir hizmet sorumlunuz yoksa [hizmet sorumlusu oluşturun](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="c50ee-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="c50ee-116">Hizmet sorumlusu ile oturum açın.</span><span class="sxs-lookup"><span data-stu-id="c50ee-116">Log in with the service principal.</span></span>

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="c50ee-117">TenantId’nizi almak için etkileşimli olarak oturum açın ve aboneliğinizden TenantId’yi edinin.</span><span class="sxs-lookup"><span data-stu-id="c50ee-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="c50ee-118">Başka bir bulut oturumu açma</span><span class="sxs-lookup"><span data-stu-id="c50ee-118">Log in to another Cloud</span></span>

<span data-ttu-id="c50ee-119">Azure Cloud Services, devletlerin veri işleme düzenlemelerine uygun farklı ortamlar sunar.</span><span class="sxs-lookup"><span data-stu-id="c50ee-119">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="c50ee-120">Azure hesabınız kamu bulutlarından birindeyse oturum açtığınızda ilgili ortamı belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c50ee-120">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="c50ee-121">Örneğin hesabınız Çin bulutundaysa şu komutla oturum açmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="c50ee-121">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="c50ee-122">Kullanabileceğiniz ortamların listesine ulaşmak için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="c50ee-122">Use the following command to get a list of available environments:</span></span>

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="c50ee-123">Azure rol tabanlı erişimi yönetme hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="c50ee-123">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="c50ee-124">Azure’da kimlik doğrulama ve abonelik yönetimi hakkında daha fazla bilgi edinmek için bkz. [Hesapları, Abonelikleri ve Yönetici Rollerini Yönetme](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="c50ee-124">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="c50ee-125">Rol yönetimi için Azure PowerShell cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="c50ee-125">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="c50ee-126">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c50ee-126">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="c50ee-127">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c50ee-127">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="c50ee-128">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c50ee-128">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="c50ee-129">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c50ee-129">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="c50ee-130">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c50ee-130">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="c50ee-131">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c50ee-131">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="c50ee-132">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c50ee-132">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
