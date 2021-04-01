---
title: Úrræðaleit fyrir vöruhúsavinnu
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsavinnu í Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: b1814f7b23efda2cabdb7bfc7bea4de6e3d6ec2f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237060"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="dbbad-103">Úrræðaleit fyrir vöruhúsavinnu</span><span class="sxs-lookup"><span data-stu-id="dbbad-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbbad-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsavinnu í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dbbad-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="dbbad-105">Ekki er hægt að færa númeraplötur sem eru með raðnúmer þegar auðir reitir og auð innhreyfing eru leyfð í rakningarvíddarflokknum.</span><span class="sxs-lookup"><span data-stu-id="dbbad-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dbbad-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="dbbad-106">Issue description</span></span>

<span data-ttu-id="dbbad-107">Ekki er hægt að færa númeraplötu með því að nota valmyndaratriðið **Hreyfing** ef raðnúmerið er með stillingar fyrir *Auð úthreyfing heimil* og *Auð innhreyfing heimil* í rakningarvíddaflokki, og ef margar númeraplötur eru á sömu staðsetningu þar sem sumar eru með raðnúmer og sumar þeirra ekki.</span><span class="sxs-lookup"><span data-stu-id="dbbad-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dbbad-108">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="dbbad-108">Issue resolution</span></span>

<span data-ttu-id="dbbad-109">Þetta vandamál verður lagfært með breytingum sem eru virkjaðar í [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span><span class="sxs-lookup"><span data-stu-id="dbbad-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="dbbad-110">Þessar breytingar gera reitinn **Raðnúmer** valfrjálsan þegar auð kvittun og auðir reitir eru leyfð.</span><span class="sxs-lookup"><span data-stu-id="dbbad-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="dbbad-111">Ég fæ eftirfarandi villuboð í vöruhúsaforritinu þegar ég keyri hreyfingar: „Birgðaeigandinn %1 er ekki leyfður í þessu ferli.“</span><span class="sxs-lookup"><span data-stu-id="dbbad-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="dbbad-112">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="dbbad-112">Issue description</span></span>

<span data-ttu-id="dbbad-113">Rakningarvíddin **Eigandi** er ekki til staðar þegar vöruhúsaforritið er notað fyrir hreyfingar.</span><span class="sxs-lookup"><span data-stu-id="dbbad-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="dbbad-114">Regluleg birgðaflutningsfærslubók úr biðlara Supply Chain Management virðist ekki virka eins og ætlað var og aðeins er hægt að bóka hana ef víddin **Eigandi** er fyllt út.</span><span class="sxs-lookup"><span data-stu-id="dbbad-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dbbad-115">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="dbbad-115">Issue resolution</span></span>

<span data-ttu-id="dbbad-116">Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika.</span><span class="sxs-lookup"><span data-stu-id="dbbad-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="dbbad-117">Sem stendur styður vöruhúsakerfisferli aðeins birgðir sem eru í eigu lögaðilans.</span><span class="sxs-lookup"><span data-stu-id="dbbad-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]