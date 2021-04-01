---
title: Úrræðaleit fyrir uppfærslu og flutning yfir í ítarlega vöruhúsastjórnun
description: Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við uppfærslu og flutning í ítarlega vöruhúsastjórnun.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f5bfee31ce27e919086f978fb3ff88ca61a65eba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208088"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="bc9ee-103">Úrræðaleit fyrir uppfærslu og flutning yfir í ítarlega vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="bc9ee-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc9ee-104">Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við uppfærslu og flutning í ítarlega vöruhúsastjórnun.</span><span class="sxs-lookup"><span data-stu-id="bc9ee-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="bc9ee-105">Ég fæ eftirfarandi villuboð: "java.security.cert.certPathValidatorException: Traustakkeri fyrir slóð vottorðs finnst ekki."</span><span class="sxs-lookup"><span data-stu-id="bc9ee-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bc9ee-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="bc9ee-106">Issue description</span></span>

<span data-ttu-id="bc9ee-107">Þessi villuboð birtast í vöruhúsaforriti vegna þess að sjálfsafgreiddum skírteinum er ekki treyst á Android 8 + í innanhússumhverfi.</span><span class="sxs-lookup"><span data-stu-id="bc9ee-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bc9ee-108">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="bc9ee-108">Issue resolution</span></span>

<span data-ttu-id="bc9ee-109">Nota ytri (opinberan) útgefanda vottorðs (CA).</span><span class="sxs-lookup"><span data-stu-id="bc9ee-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="bc9ee-110">Lausn fyrir þetta vandamál er í boði í útgáfu 1.9.0.0 af vöruhúsaforritinu.</span><span class="sxs-lookup"><span data-stu-id="bc9ee-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="bc9ee-111">Frekari upplýsingar um þetta vandamál og hvernig á að laga það er að finna á [Úrræðaleit vegna vandamála með tengingu í vöruhúsaforriti](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bc9ee-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="bc9ee-112">Hvert er samþykkt ferli fyrir flutning úr grunnvöruhús í ítarlegt vöruhús?</span><span class="sxs-lookup"><span data-stu-id="bc9ee-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="bc9ee-113">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="bc9ee-113">Issue description</span></span>

<span data-ttu-id="bc9ee-114">Verið er að keyra lager-/birgðastjórnun og nota grunnstillingu lagers og færa á ítarlegt vöruhús til að nýta fartæki, bylgjur og vinnu.</span><span class="sxs-lookup"><span data-stu-id="bc9ee-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="bc9ee-115">Hins vegar kemur upp vandamál þegar reynt er að færa þetta.</span><span class="sxs-lookup"><span data-stu-id="bc9ee-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="bc9ee-116">Til dæmis er ekki hægt að breyta afurðum þannig að þær noti geymsluvíddir (svæði, vöruhús og staðsetning) vegna þess að afurðirnar eru með færslur á móti þeim.</span><span class="sxs-lookup"><span data-stu-id="bc9ee-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="bc9ee-117">Þess vegna þarf að læra samþykkt ferli fyrir flutning frá grunnvöruhúsi í ítarlegt vöruhús.</span><span class="sxs-lookup"><span data-stu-id="bc9ee-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bc9ee-118">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="bc9ee-118">Issue resolution</span></span>

<span data-ttu-id="bc9ee-119">Frekari upplýsingar um ferlið fyrir flutning frá grunnvöruhúsi í ítarlegt vöruhús er að finna í eftirfarandi bloggfærslum og fylgiskjölum:</span><span class="sxs-lookup"><span data-stu-id="bc9ee-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="bc9ee-120">Virkja ferli vöruhúsastjórnunar fyrir fyrirliggjandi vörur og vöruhús</span><span class="sxs-lookup"><span data-stu-id="bc9ee-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="bc9ee-121">Flutningur á Microsoft Dynamics AX WMS í ný R3 vöruhús og flutningsvirkni</span><span class="sxs-lookup"><span data-stu-id="bc9ee-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="bc9ee-122">WMSI/WMS2 atriðaflutningur</span><span class="sxs-lookup"><span data-stu-id="bc9ee-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="bc9ee-123">Uppfæra vöruhúsastjórnunarferli úr Microsoft Dynamics AX 2012 í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="bc9ee-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]