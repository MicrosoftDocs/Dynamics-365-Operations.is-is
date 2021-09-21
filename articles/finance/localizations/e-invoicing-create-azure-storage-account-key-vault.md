---
title: Setja upp Azure-geymslureikning og lyklageymslu
description: Í þessu efnisatriði er útskýrt hvernig á að stofna Azure-geymslureikning og lyklageymslu.
author: gionoder
ms.date: 08/17/2021
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
ms.openlocfilehash: 23fec7a00d800719e1a7d2c90f9d0977d56be038
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463858"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Setja upp Azure-geymslureikning og lyklageymslu

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að ljúka við skrefin í þessu efnisatriði þarf að ganga úr skugga um að eftirfarandi verkum sé lokið:

- Stofna lyklageymslutilfang í Azure. Frekari upplýsingar er að finna í [Um Azure-lyklageymslu](/azure/key-vault/general/overview).
- Stofna Azure-geymslureikning (Blob-geymsla). Frekari upplýsingar er að finna í [Unnið með Azure-geymslureikning](/azure/storage/blobs/).

## <a name="overview"></a>Yfirlit

Í þessu efnisatriði verður farið í gegnum tvö aðalskref:

- Setja skal upp Azure-geymslureikning til að fá URI geymslureiknings.
- Setja skal upp lyklageymslu til að geyma URI geymslureiknings.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Setja upp Azure-geymslureikning til að fá URI geymslureiknings

1. Opnið geymslureikninginn sem ætlunin er að nota með rafrænni reikningsfærslu.
2. Farið í **Gagnageymslu** > **Geymslur** og stofnið nýja geymslu.
3. Sláið inn nafn geymslunnar og stillið reitinn **Almennt aðgangsstig** á **Einkaaðili (enginn nafnlaus aðgangur)**.
4. Opnið geymsluna og farið í **Stillingar** > **Aðgangsregla**.
5. Veljið **Bæta við reglu** til að bæta við geymdri aðgangsreglu.
6. Stillið reitina **Kennimerki** og **Aðgangsheimildir** eftir því sem við á. Í reitnum **Aðgangsheimildir** á að velja allar aðgangsheimildir.

    ![Aðgangsheimild Blob-geymslu veitt.](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Færið inn upphafs-og lokadagsetningar. Lokadagsetningin á að vera fram í tímann.
8. Veljið **Í lagi** til að vista regluna og vistið síðan breytingarnar í geymsluna.
9. Farið í **Stillingar** > **Samnýttir aðgangslyklar** og stillið gildin í reitnum. 
10. Færið inn upphafs- og lokadagsetningar. Lokadagsetningin á að vera fram í tímann.
11. Í reitnum **Heimildir** skal velja eftirfarandi heimildir: **Lesa**, **Bæta við**, **Búa til**, **Skrifa**, **Eyða** og **Listi**. 
12. Veljið **Mynda SAS-merki og vefslóð**.
13. Afritaðu og geymdu gildið í reitnum **Blob SAS-vefslóð**. Þetta gildi verður notað í næsta ferli og verður vísað til þess sem *URI-undirskrift samnýtts aðgangs*.

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Setja skal upp lyklageymslu til að geyma URI geymslureiknings

1. Opnið lyklageymsluna sem ætlunin er að nota með rafrænni reikningsfærslu.
2. Farið í **Stillingar** \> **Leynilyklar** og veljið síðan **Búa til/Flytja inn** til að stofna nýjan leynilykil.
3. Á síðunni **Stofna leynilykil**, í reitnum **Valkostir upphleðslu**, skal velja **Handvirkt**.
4. Færið inn heiti leynilykilsins. Þetta heiti verður notað við uppsetningu þjónustunnar í Regulatory Configuration Service (RCS) og verður vísað í það sem *leyniheiti lyklageymslu*.
5. Í reitinn **Gildi** skal færa inn URI undirskrift samnýtts aðgangs sem þú afritaðir í fyrra ferlinu og veldu því næst **Búa til**.
6. Setja upp aðgangsregluna til að veita rafrænu reikningsfærslunni rétt öryggisstig aðgangs að leynilyklinum sem var búinn til. Opnið **Stillingar \> Aðgangsregla** og veljið **Bæta við aðgangsreglu**.
7. Stillið aðgangsheimildir leynilykils fyrir aðgerðirnar **Fá** og **Listi**.

    ![Veita aðgang að þjónustu.](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Stillið heimildir vottorðsins fyrir aðgerðirnar **Fá** og **Listi**.

    ![Vottorðsheimild veitt.](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Í reitnum **Velja aðalreikning** skal velja **Ekkert valið**.
10. Í svarglugganum **Aðalreikningur** skal velja aðalreikninginn með því að bæta við **Þjónusta rafrænnar reikningsfærslu**.
11. Veljið **Bæta við** og veljið síðan **Vista**.
12. Á síðunni **Yfirlit** skal afrita **DNS-heiti** fyrir lyklageymslu. Þetta gildi verður notað við uppsetningu þjónustunnar í RCS og verður vísað í sem *URI lyklageymslu*.

> [!NOTE]
> Fyrir viðbótaröryggi á geymslureikningi skal skilgreina Azure Defender fyrir geymslu.
> 
> Frekari upplýsingar er að finna í [Kynning á Azure Defender fyrir geymslu](/azure/security-center/defender-for-storage-introduction).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
