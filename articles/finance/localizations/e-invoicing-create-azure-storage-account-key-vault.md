---
title: Setja upp Azure-geymslureikning og lyklageymslu
description: Í þessu efnisatriði er útskýrt hvernig á að stofna Azure-geymslureikning og lyklageymslu.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: d076aa5230437d1ef90f6b46d49ee4dea526db24
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104230"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Setja upp Azure-geymslureikning og lyklageymslu

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að ljúka við skrefin í þessu efnisatriði þarf að ganga úr skugga um að eftirfarandi verkum sé lokið:

- Stofna lyklageymslutilfang í Azure. Frekari upplýsingar er að finna í [Um Azure-lyklageymslu](https://docs.microsoft.com/azure/key-vault/general/overview).
- Stofna Azure-geymslureikning (Blob-geymsla). Frekari upplýsingar er að finna í [Unnið með Azure-geymslureikning](https://docs.microsoft.com/azure/storage/blobs/).

## <a name="overview"></a>Yfirlit

Í þessu efnisatriði verður farið í gegnum tvö aðalskref:

- Setja skal upp Azure-geymslureikning til að fá URI geymslureiknings.
- Setja skal upp lyklageymslu til að geyma URI geymslureiknings.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Setja upp Azure-geymslureikning til að fá URI geymslureiknings

1. Opnið geymslureikninginn sem ætlunin er að nota með viðbót rafrænnar reikningsfærslu.
2. Farið í **Blog-þjónusta** \> **Geymsla** og stofnið nýja geymslu.
3. Sláið inn nafn geymslunnar og stillið reitinn **Almennt aðgangsstig** á **Einkaaðili (enginn nafnlaus aðgangur)**.
4. Opnið geymsluna og farið í **Stillingar \> Aðgangsregla**.
5. Veljið **Bæta við reglu** til að bæta við geymdri aðgangsreglu.
6. Stillið reitina **Kennimerki** og **Aðgangsheimildir** eftir því sem við á. Í reitnum **Aðgangsheimildir** á að velja allar aðgangsheimildir.

    ![Aðgangsheimild Blob-geymslu veitt](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Færið inn upphafs-og lokadagsetningar. Lokadagsetningin á að vera fram í tímann.
8. Veljið **Í lagi** til að vista regluna og vistið síðan breytingarnar í geymsluna.
9. Farið aftur í geymslureikninginn og opnið **Geymsluskoðara (forútgáfa)**.
10. Hægrismellið á geymsluna og veljið síðan **Fá undirskrift samnýtts aðgangs**.
11. Í svarglugganum **Undirskrift samnýtts aðgangs** skal afrita og vista gildin í reitnum **URI**. Þetta gildi verður notað í næsta ferli og verður vísað til þess sem *URI-undirskrift samnýtts aðgangs*.

    ![URI-gildin valin og afrituð](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Setja skal upp lyklageymslu til að geyma URI geymslureiknings

1. Opnið lyklageymsluna sem ætlunin er að nota með viðbót rafrænnar reikningsfærslu.
2. Farið í **Stillingar** \> **Leynilyklar** og veljið síðan **Búa til/Flytja inn** til að stofna nýjan leynilykil.
3. Á síðunni **Stofna leynilykil**, í reitnum **Valkostir upphleðslu**, skal velja **Handvirkt**.
4. Færið inn heiti leynilykilsins. Þetta heiti verður notað við uppsetningu þjónustunnar í Regulatory Configuration Service (RCS) og verður vísað í það sem *leyniheiti lyklageymslu*.
5. Í reitnum **Gildi** skal velja **URI-undirskrift samnýtts aðgangs** og veljið síðan **Stofna**.
6. Setja upp aðgangsregluna til að veita rafrænu reikningsfærsluviðbótinni rétt öryggisstig aðgangs að leynilyklinum sem var búinn til. Opnið **Stillingar \> Aðgangsregla** og veljið **Bæta við aðgangsreglu**.
7. Stillið aðgangsheimildir leynilykils fyrir aðgerðirnar **Fá** og **Listi**.

    ![Veita aðgang að þjónustu](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Stillið heimildir vottorðsins fyrir aðgerðirnar **Fá** og **Listi**.

    ![Vottorðsheimildir veittar](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Í svarglugganum **Aðalreikningur** skal velja aðalreikninginn með því að bæta við **Viðbót rafrænnar reikningsfærslu**.
10. Veljið **Bæta við** og veljið síðan **Vista breytingar lyklageymslu**.
11. Á síðunni **Yfirlit** skal afrita **DNS-heiti** fyrir lyklageymslu. Þetta gildi verður notað við uppsetningu þjónustunnar í RCS og verður vísað í sem *URI lyklageymslu*.
