---
title: TDS-útreikningur á reikningum af síðu reiknings með frjálsum texta
description: Í þessu efnisatriði er útskýrt hvernig á að reikna út skatt sem dreginn er frá upprunalegri greiðslu (TDS) á reikningum með því að nota síðu reiknings með frjálsum texta.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023334"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>TDS-útreikningur á reikningum af síðu reiknings með frjálsum texta

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að reikna út skatt sem dreginn er frá upprunalegri greiðslu (TDS) á reikningum með því að nota síðuna **Reikningur með frjálsum texta**.

1. Fara í **Viðskiptakröfur \> Reikningar \> Allir reikningar með frjálsum texta**.

    [![Síða reiknings með frjálsum texta](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. Veljið **Nýr** til að stofna nýjan reikning með frjálsum texta og færið inn nauðsynlegar upplýsingar.
3. Veljið flipann **Reikningur**. Í hlutanum **Staðgreiðsluskattsflokkur** sýnir reiturinn **Eðli skattgreiðanda** eðli skattgreiðendaflokks viðskiptavinar.
4. Í reitnum **TDS-flokkur** skal yfirfara og breyta sjálfgefnum TDS-flokki sem er skilgreindur fyrir viðskiptavininn.

    > [!NOTE]
    > Þegar gildi er valið í reitnum **TDS-flokkur** verður reiturinn **TCS-flokkur** óaðgengilegur. TDS er aðeins reiknað ef valkosturinn **Reikna staðgreiðsluskatt** er stilltur á **Já** fyrir viðskiptavininn á síðunni **Allir viðskiptavinir**.

5. Í flipanum **Skattaupplýsingar**, í hlutanum **Upplýsingar um fyrirtæki**, í reitnum **Heiti**, skal velja heiti fyrirtækis fyrir aukaaðsetur sem hefur verið sett upp fyrir fyrirtækið.

    Í hlutanum **Staðgreiðsluskattur** sýnir reiturinn **Skattlykilnúmer (TAN)** skattlykilnúmer (TAN) fyrir valið fyrirtæki.

6. Í flipanum **Reikningslínur** skal stofna reikningslínur og færa inn nauðsynlegar upplýsingar.

    Í hlutanum **Staðgreiðsluskattsflokkur** sýnir reiturinn **Skattlykilnúmer (TAN)** TAN og reiturinn **TDS-flokkur** sýnir TDS-flokkinn.

7. Veljið **Staðgreiðsluskattur** til að opna síðuna **Tímabundnar staðgreiðsluskattsfærslur**. Efri hluti þessarar síðu hefur eftirfarandi reiti:

    - **Upphæð staðgreiðsluskatts samtals** - Samtals TDS sem var reiknað út fyrir færsluna fyrir TDS-flokkinn.
    - **Gildi** - Heildarprósenta sem var notuð til að reikna út TDS fyrir færsluna. Heildarprósentan er byggð á formúlunni sem er skilgreind fyrir TDS-skattkóða og hengd við TDS-flokkinn.
    - **Samtals leiðrétt upphæð staðgreiðsluskatts** – Leiðrétt heildarupphæð TDS fyrir alla skattkóða í TDS-flokknum.
    - **TDS** – Valinn gátreitur gefur til kynna að TDS-flokkurinn er hengdur við færsluna.

    Reitirnir í flipunum **Yfirlit**, **Almennt** og **Leiðrétting** sýna reiknaða upphæð TDS og upplýsingar um leiðrétta TDS-upphæð fyrir hvern TDS-skattkóða sem er hengdur við TDS-flokkinn.

8. Veljið **Mörk** til að opna síðuna **Mörk** þar sem hægt er að fara yfir hámarkið sem er skilgreint fyrir TDS-skatthluta sem er hengdur við tiltekinn TDS-skattkóða.
9. Veldu **Formúluhönnuður** til að opna síðuna **Formúluhönnuður** þar sem hægt er að fara yfir formúluna sem er skilgreind fyrir tiltekinn TDS-skattkóða.
10. Bóka textareikning. TDS-upphæðin sem reiknuð er fyrir reikning með frjálsum texta er bókuð á lykil viðskiptakrafa sem er skilgreindur fyrir hvern TDS-skattkóða í TDS-flokknum. Lyklar viðskiptakrafa fyrir TDS-skattkóða eru skilgreindir á síðunni **Staðgreiðsluskattskóðar**.
11. Veljið **Bókaður staðgreiðsluskattur** til að opna síðuna **Staðgreiðsluskattsfærslur**. Reiturinn **Gildi** sýnir heildarprósentuna sem var notuð til að reikna út TDS fyrir færsluna.

    Reitirnir í flipunum **Yfirlit**, **Almennt** og **Upphæð** sýna TDS-upphæðirnar sem voru reiknaðar í reikningslínunum.

12. Farið yfir upplýsingar um útreikning TDS fyrir hvern TDS-skattkóða sem hengdur er við TDS-flokkinn.
