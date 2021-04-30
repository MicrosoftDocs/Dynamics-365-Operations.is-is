---
title: Setja upp Azure-geymslureikning og lyklageymslu
description: Í þessu efnisatriði er útskýrt hvernig á að stofna Azure-geymslureikning og lyklageymslu.
author: gionoder
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 2786d350fde2399aadb35dc653bc15123e0e6d91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893803"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="36d60-103">Setja upp Azure-geymslureikning og lyklageymslu</span><span class="sxs-lookup"><span data-stu-id="36d60-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="36d60-104">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="36d60-104">Prerequisites</span></span>

<span data-ttu-id="36d60-105">Áður en hægt er að ljúka við skrefin í þessu efnisatriði þarf að ganga úr skugga um að eftirfarandi verkum sé lokið:</span><span class="sxs-lookup"><span data-stu-id="36d60-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="36d60-106">Stofna lyklageymslutilfang í Azure.</span><span class="sxs-lookup"><span data-stu-id="36d60-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="36d60-107">Frekari upplýsingar er að finna í [Um Azure-lyklageymslu](/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="36d60-107">For more information, see [About Azure Key Vault](/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="36d60-108">Stofna Azure-geymslureikning (Blob-geymsla).</span><span class="sxs-lookup"><span data-stu-id="36d60-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="36d60-109">Frekari upplýsingar er að finna í [Unnið með Azure-geymslureikning](/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="36d60-109">For more information, see [Maintaining Azure Storage Account](/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="36d60-110">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="36d60-110">Overview</span></span>

<span data-ttu-id="36d60-111">Í þessu efnisatriði verður farið í gegnum tvö aðalskref:</span><span class="sxs-lookup"><span data-stu-id="36d60-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="36d60-112">Setja skal upp Azure-geymslureikning til að fá URI geymslureiknings.</span><span class="sxs-lookup"><span data-stu-id="36d60-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="36d60-113">Setja skal upp lyklageymslu til að geyma URI geymslureiknings.</span><span class="sxs-lookup"><span data-stu-id="36d60-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="36d60-114">Setja upp Azure-geymslureikning til að fá URI geymslureiknings</span><span class="sxs-lookup"><span data-stu-id="36d60-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="36d60-115">Opnið geymslureikninginn sem ætlunin er að nota með rafrænni reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="36d60-115">Open the storage account that you plan to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="36d60-116">Farið í **Blog-þjónusta** \> **Geymsla** og stofnið nýja geymslu.</span><span class="sxs-lookup"><span data-stu-id="36d60-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="36d60-117">Sláið inn nafn geymslunnar og stillið reitinn **Almennt aðgangsstig** á **Einkaaðili (enginn nafnlaus aðgangur)**.</span><span class="sxs-lookup"><span data-stu-id="36d60-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="36d60-118">Opnið geymsluna og farið í **Stillingar \> Aðgangsregla**.</span><span class="sxs-lookup"><span data-stu-id="36d60-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="36d60-119">Veljið **Bæta við reglu** til að bæta við geymdri aðgangsreglu.</span><span class="sxs-lookup"><span data-stu-id="36d60-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="36d60-120">Stillið reitina **Kennimerki** og **Aðgangsheimildir** eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="36d60-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="36d60-121">Í reitnum **Aðgangsheimildir** á að velja allar aðgangsheimildir.</span><span class="sxs-lookup"><span data-stu-id="36d60-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Aðgangsheimild Blob-geymslu veitt](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="36d60-123">Færið inn upphafs-og lokadagsetningar.</span><span class="sxs-lookup"><span data-stu-id="36d60-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="36d60-124">Lokadagsetningin á að vera fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="36d60-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="36d60-125">Veljið **Í lagi** til að vista regluna og vistið síðan breytingarnar í geymsluna.</span><span class="sxs-lookup"><span data-stu-id="36d60-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="36d60-126">Farið aftur í geymslureikninginn og opnið **Geymsluskoðara (forútgáfa)**.</span><span class="sxs-lookup"><span data-stu-id="36d60-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="36d60-127">Hægrismellið á geymsluna og veljið síðan **Fá undirskrift samnýtts aðgangs**.</span><span class="sxs-lookup"><span data-stu-id="36d60-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="36d60-128">Í svarglugganum **Undirskrift samnýtts aðgangs** skal afrita og vista gildin í reitnum **URI**.</span><span class="sxs-lookup"><span data-stu-id="36d60-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="36d60-129">Þetta gildi verður notað í næsta ferli og verður vísað til þess sem *URI-undirskrift samnýtts aðgangs*.</span><span class="sxs-lookup"><span data-stu-id="36d60-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![URI-gildin valin og afrituð](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="36d60-131">Setja skal upp lyklageymslu til að geyma URI geymslureiknings</span><span class="sxs-lookup"><span data-stu-id="36d60-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="36d60-132">Opnið lyklageymsluna sem ætlunin er að nota með rafrænni reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="36d60-132">Open the key vault that you intend to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="36d60-133">Farið í **Stillingar** \> **Leynilyklar** og veljið síðan **Búa til/Flytja inn** til að stofna nýjan leynilykil.</span><span class="sxs-lookup"><span data-stu-id="36d60-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="36d60-134">Á síðunni **Stofna leynilykil**, í reitnum **Valkostir upphleðslu**, skal velja **Handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="36d60-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="36d60-135">Færið inn heiti leynilykilsins.</span><span class="sxs-lookup"><span data-stu-id="36d60-135">Enter the name of the secret.</span></span> <span data-ttu-id="36d60-136">Þetta heiti verður notað við uppsetningu þjónustunnar í Regulatory Configuration Service (RCS) og verður vísað í það sem *leyniheiti lyklageymslu*.</span><span class="sxs-lookup"><span data-stu-id="36d60-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="36d60-137">Í reitnum **Gildi** skal velja **URI-undirskrift samnýtts aðgangs** og veljið síðan **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="36d60-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="36d60-138">Setja upp aðgangsregluna til að veita rafrænu reikningsfærslunni rétt öryggisstig aðgangs að leynilyklinum sem var búinn til.</span><span class="sxs-lookup"><span data-stu-id="36d60-138">Set up the access policy to grant Electronic invoicing the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="36d60-139">Opnið **Stillingar \> Aðgangsregla** og veljið **Bæta við aðgangsreglu**.</span><span class="sxs-lookup"><span data-stu-id="36d60-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="36d60-140">Stillið aðgangsheimildir leynilykils fyrir aðgerðirnar **Fá** og **Listi**.</span><span class="sxs-lookup"><span data-stu-id="36d60-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Veita aðgang að þjónustu](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="36d60-142">Stillið heimildir vottorðsins fyrir aðgerðirnar **Fá** og **Listi**.</span><span class="sxs-lookup"><span data-stu-id="36d60-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Vottorðsheimildir veittar](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="36d60-144">Í reitnum **Velja aðalreikning** skal velja **Ekkert valið**.</span><span class="sxs-lookup"><span data-stu-id="36d60-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="36d60-145">Í svarglugganum **Aðalreikningur** skal velja aðalreikninginn með því að bæta við **Þjónusta rafrænnar reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="36d60-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="36d60-146">Veljið **Bæta við** og veljið síðan **Vista breytingar lyklageymslu**.</span><span class="sxs-lookup"><span data-stu-id="36d60-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="36d60-147">Á síðunni **Yfirlit** skal afrita **DNS-heiti** fyrir lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="36d60-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="36d60-148">Þetta gildi verður notað við uppsetningu þjónustunnar í RCS og verður vísað í sem *URI lyklageymslu*.</span><span class="sxs-lookup"><span data-stu-id="36d60-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]