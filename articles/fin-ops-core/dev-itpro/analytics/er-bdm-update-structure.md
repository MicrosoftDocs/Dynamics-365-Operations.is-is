---
title: Uppfæra skipan sniðmáts viðskiptaskjals
description: Þetta efnisatriði útskýrir hvernig á að uppfæra skipulag sniðmáts viðskiptaskjals með því að nota eiginleikann stjórnun viðskiptaskjala.
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 203c9f0990051c1618660959dad0e184add68ffa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750485"
---
# <a name="update-the-structure-of-a-business-document-template"></a>Uppfæra skipan sniðmáts viðskiptaskjals 

[!include[banner](../includes/banner.md)]

Á glugganum **Skipulag sniðmáts** í sniðmátsritlinum [Viðskiptaskjalastjórnun](er-business-document-management.md) er hægt að breyta viðskiptaskjalasniðmáti með því að [bæta við nýjum svæðum](er-bdm-add-field-to-excel-template.md) á sniðmát í Microsoft Excel. Skipulag sniðmátsins er síðan sjálfkrafa uppfært í Dynamics 365 Finance þannig að það endurspegli breytingarnar sem gerðar voru í glugganum **Skipulag sniðmáts**.

Einnig er hægt að breyta sniðmáti með því að nota Office 365 neteiginleikann. Til dæmis er hægt að bæta við nýju atriði með heiti, t.d. mynd eða lögun, á breytanlega vinnublaðið. Í þessu tilviki er skipulag sniðmátsins ekki sjálfkrafa uppfært í Finance og varan sem bætt var við birtist ekki á glugganum **Skipulag sniðmáts**. Uppfærið sniðmát handvirkt í Finance með því að velja **Uppfæra skipulag** á síðu sniðmátsritilsins.

Fyrir frekari upplýsingar um þennan eiginleika skal ljúka eftirfarandi dæmum.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Dæmi: Uppfæra skipan sniðmáts viðskiptaskjals

Þetta dæmi sýnir hvernig kerfisstjóri getur uppfært uppbyggingu sniðmáts viðskiptaskjals í Finance eftir að sniðmátinu er breytt í Office Online. Eftirfarandi kaflar útskýra skrefin sem um er að ræða.

### <a name="prepare-a-business-document-template-for-editing"></a>Undirbúa sniðmát viðskiptaskjals fyrir breytingar

Ljúkið eftirfarandi ferli í [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).

1. [Skilgreina færibreytur Rafræn skýrslugerðar](er-business-document-management.md#configure-er-parameters)
2. [Flytja inn ER-lausnir](er-business-document-management.md#import-er-solutions)
3. [Virkja stjórnun viðskiptaskjala](er-business-document-management.md#enable-business-document-management)
4. [Skilgreina færibreytur](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>Breyta sniðmáti viðskiptaskjala

1. Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.
2. Á síðunni **Búa til nýtt sniðmát** skal velja sniðmátið **Reikningur með frjálsum texta (rafrænt skýrslugerðardæmi)(Excel)**.
3. Veljið **Búa til skjal**.
4. Á svæðinu **Titill** skal slá inn **Dæmi um reikning með frjálsum texta fyrir Litware**.
5. Veljið **Í LAGI** til að stofna nýja sniðmátið.

    > [!NOTE]
    > Ef notandinn hefur ekki enn skráð sig inn á Office Online er honum [beint á Office 365 innskráningarsíðuna](er-business-document-management.md#frequently-asked-questions). Til að fara aftur í fjármálaumhverfið skal velja hnappinn **Til baka** í vafranum.

    Nýja sniðmátið er opnað fyrir breytingar í Excel Online innbyggðu stýringunni á sniðmátssíðu.

[![Nota vinnusvæði stjórnunar vinnuskjala til að hefja breytingar á sniðmáti viðskiptaskjals](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>Yfirfara núverandi byggingu breytanlegs sniðmáts

1. Í Excel Online, á borðanum, á flipanum **Yfirlit**, í flokknum **Sýna**, skal velja **Hnitalínur**.
2. Í breytanlegu sniðmáti skal velja rétthyrninginn fyrir ofan titil sniðmátsins. Þessi rétthyrningur er mynd sem nefnist **rptHeaderCompLogo**.
3. Ef **Skipulag sniðmáts** svæðið er falið , skal velja **Sýna skipulag**.
4. Á glugganum **Skipulag sniðmáts** skal stækka **Skýrsla \> Reikningur \> rptHeader \> rptHeaderPart1**.
5. Takið eftir að, í sniðmátsuppbyggingu í Finance, er **rptHeaderCompLogo**-varan birt sem undireining **Skýrsla \> Reikningur \> rptHeader \> rptHeaderPart1**.

[![Vinnusvæði viðskiptaskjalastjórnunar notað til að yfirfara núverandi uppbyggingu breytanlegs sniðmáts](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>Uppfæra skipan sniðmáts viðskiptaskjals með því að eyða mynd

1. Í Excel online, í breytanlegu sniðmáti, skal velja **rptHeaderCompLogo** myndina.
2. Fylgdu einu af þessum skrefum til að eyða valinni mynd úr breytanlegu sniðmáti:

    - Veljið **DELETE** lykilinn á lyklaborðinu.
    - Veljið og haldið fingri (eða hægrismellið) á myndina og veljið síðan **Klippa**.

    > [!NOTE]
    > Atriðið **rptHeaderCompLogo** er enn til staðar í skipulagi sniðmáts í Fjármálum, jafnvel þótt myndin sé ekki lengur innifalin í Excel-sniðmátinu.

3. Veljið **Uppfæra skipulag** til að samstilla byggingu breytanlegra sniðmáta í Excel og Finance.
4. Á glugganum **Skipulag sniðmáts** skal stækka **Skýrsla \> Reikningur \> rptHeader \> rptHeaderPart1**.
5. Takið eftir því að **rptHeaderCompLogo** varan er ekki lengur með í sniðmátsuppbyggingu í Finance.

[![Nota vinnusvæði stjórnunar vinnuskjala til að eyða mynd úr sniðmáti viðskiptaskjals](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>Uppfæra skipan sniðmáts viðskiptaskjals með því að bæta við mynd

1. Á Excel Online á borða flipans **Setja inn** í flokkinum **Myndskreytingar** skal velja **Mynd**.
2. Veldu **Velja skrá**, flettu að myndinni sem þú vilt bæta við, veldu hana og veldu svo **Í lagi**.
3. Veljið **Setja inn**.
4. Færðu nýju myndin þar til hún er á réttum stað. Sjálfgefið er að Excel gefi myndinni heiti. Til dæmis gæti það gefið myndinni heitið **Mynd 2**.
5. Veljið **Uppfæra skipulag** til að samstilla byggingu breytanlegra sniðmáta í Excel og Finance.
6. Á glugganum **Skipulag sniðmáts** skal stækka **Skýrsla \> Reikningur \> rptHeader \> rptHeaderPart1**.
7. Takið eftir að nýja myndin er nú tekin með sem vara í sniðmátsuppbyggingu í Finance.

[![Nota vinnusvæði stjórnunar vinnuskjala til að bæta mynd við sniðmát viðskiptaskjals](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>Tengdir tenglar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]