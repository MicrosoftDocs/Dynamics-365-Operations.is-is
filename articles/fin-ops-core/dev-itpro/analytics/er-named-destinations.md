---
title: Skilgreina færslutengda áfangastaði rafrænnar skýrslugerðar fyrir prentstýringu
description: Þessi grein útskýrir hvernig á að stilla prentstjórnunarfærslu tiltekna áfangastaði fyrir rafræn skýrslugerð (ER) snið sem er stillt til að búa til skjöl á útleið.
author: kfend
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7c92d580f6adebdba12b7964a42fd4752e9c9205
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285062"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Skilgreina færslutengda áfangastaði rafrænnar skýrslugerðar fyrir prentstýringu

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig notandi í hlutverki kerfisstjóra eða viðskiptakrafa getur framkvæmt eftirfarandi verkefni:

- Skilgreindu nefnda áfangastaði [Rafrænnar skýrslugerðar](general-electronic-reporting.md) fyrir lausn rafrænnar skýrslugerðar sem myndar reikniga með frjálsum texta.
- Úthlutaðu áfangastað rafrænnar skýrslugerðar á eina færslu [prentstýringar](document-reporting-services.md).

Hægt er að ljúka ferlinu í USMF-fyrirtækinu. Ekki er þörf á neinni kóðun.

## <a name="introduction"></a>Kynning

Hægt er að skilgreina [áfangastaði](electronic-reporting-destinations.md) fyrir hverja möppu í úttakshluta möppu fyrir [skilgreiningu](general-electronic-reporting.md) á [sniði](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar sem er notað til að mynda skjal á útleið. Þegar þú keyrir snið rafrænnar skýrslugerðar af þessari gerð og ert með viðeigandi aðgangsréttindi geturðu einnig breytt stillingum skilgreinds áfangastaðar við keyrslu.

Í Microsoft Dynamics 365 Fjármál **útgáfu 10.0.17 og síðar**, aðgerðakóði getur verið [sett upp](er-apis-app10-0-17.md) fyrir ER snið til að tilgreina aðgerðina sem notendur framkvæma með því að keyra það ER snið. Til dæmis í einingunni **Viðskiptakröfur**, í stillingum prentstýringar, er hægt að velja snið rafrænnar skýrslugerðar sem myndar ákveðið viðskiptaskjal á borð við reikning með frjálsum texta. Síðan er hægt að velja **Skoða** til að forskoða reikning eða **Prenta** til að senda hann til prentara. Ef aðgerð er gerð fyrir keryslu á sniði rafrænnar skýrslugerðar við keyrslu er hægt að skilgreina mismunandi [áfangastaði rafrænnar skýrslugerðar fyrir mismunandi notandaaðgerðir](er-action-dependent-destinations.md).

Í Finance **útgáfu 10.0.21 og nýrri** getur nefndur áfangastaður verið [settur upp](er-apis-app10-0-21.md) fyrir snið rafrænnar skýrslugerðar og úthlutaður færslu prentstýringar sem er unnið úr þegar snið rafrænnar skýrslugerðar er keyrt. Í einingunni **Viðskiptakröfur**, í stillingum prentstýringar, viltu til að mynda skilgreina **Upprunalegu færsluna** þannig að hún framkvæmi eftirfarandi aðgerðir:

- Keyrðu snið rafrænnar skýrslugerðar.
- Sendu viðskiptavini útbúinn reikning í tölvupósti.
- Skilgreindu færsluna **Afrit** þannig að hún keyri sama sniðið.
- Prentaðu afrit af reikningnum á netprentaranum.

Í þessu tilviki verður þú að skilgreina mismunandi áfangastaði rafrænnar skýrslugerðar snið rafrænnar skýrslugerðar sem er í keyrslu og þú verður að velja áfangastaðina fyrir mismunandi færslur prentstýringar.

## <a name="prerequisites"></a>Forkröfur

Áður en þú hefst handa þarf að kveikja á eiginleikanum **Leyfa að setja upp áfangastaði rafrænnar skýrslugerðar fyrir hvert prentstýringaratriði** á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace). Einnig þarf að breyta frumkóðanum til að hægt sé að skilgreina nefnda áfangastaði rafrænnar skýrslugerðar í núverandi Finance-tilviki og til að virkja [nýja](er-apis-app10-0-21.md) API rafrænnar skýrslugerðar.

Skilgreining rafrænnar skýrslugerðar fyrir **Reikning með frjálsum texta (Excel)** verður auk þess að vera [fluttur inn](er-download-configurations-global-repo.md) í Finance-tilvikið.

## <a name="configure-a-new-er-destination"></a>Skilgreina nýjan áfangastað rafrænnar skýrslugerðar

1. Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.
2. Veldu reikning fyrir viðskiptavinalykil **US-001**.
3. Á síðunni **Reikningur með frjálsum texta**, í flipanum **Reikningur**, í hópnum **Prentstýring**, skal velja **Prentstýring**.
4. Á síðunni **Uppsetning á prentstýringu** skal útvíkka **Eining - Viðskiptakröfur** \> **Skjöl** \> **Reikningur með frjálsum texta**, velja færsluna **Upprunalegt** og síðan fylgja þessum skrefum:

    1.  Fylgstu með núverandi stillingum á valdri færslu:
        -   Sjálfgefin SSRS-skýrsla **FreeTextInvoice.Report** er valin í reitnum **Skýrslusnið**.
        -   **\<Default\>** heitið er sýnt í reitnum **Áfangastaður** sem gefur til kynna að enginn sérsniðinn áfangastaður sé valinn fyrir SSRS-skýrsluna sem var úthlutað. 
    2.  Í reitnum **Skýrslusnið** skal velja skilgreininguna **Reikningur með frjálsum texta (Excel)** fyrir rafrænt skýrslugerðarsnið.
        -   Heiti reitsins **Áfangastaður** er breytt í **Heiti áfangastaðar**.
        -   **\<No named destination\>** Heitið er sýnt í reitnum **Heiti áfangastaðar** sem gefur til kynna að enginn nefndur áfangastaður valinn fyrir rafræna skýrslugerðarsniðið sem var úthlutað.
    3.  Veldu örvarhnappinn hægra megin við reitinn **Heiti áfangastaðar**.    
    4. Á síðuna **Nefndur áfangastaður fyrir rafræna skýrslugerð**, í reitinn **Heiti**, skal slá inn **Aðaláfangastaður**.
    5. Veldu **Vista**.
    6. Í flýtiflipanum **Viðtökustaður skráar** skal [skilgreina](er-destination-type-email.md) áfangastað **Tölvupósts** fyrir **Skýrsluhlutann**.
    7. Lokaðu síðunni **Nefndur áfangastaður fyrir rafræna skýrslugerð**.
    8. Á síðunni **Uppsetning á prentstýringu**, í reitnum **Heiti áfangastaðar**, skal velja **Aðaláfangastað** fyrir nefndan áfangastað.

    ![Að skilgreina nefndan áfangastað rafrænnar skýrslugerðar fyrir valið snið rafrænnar skýrslugerðar og úthluta honum á skilgreinda færslu prentstýringar á uppsetningarsíðu prentstýringar](./media/er-named-destinations-01.gif)

    Þú hefur nú skilgreint **Aðaláfangastað** fyrir nefndan áfangastað rafrænnar skýrslugerðar fyrir sniðið **Reikningur með frjálsum texta (Excel)** og úthlutað honum á **Upprunalegu** prentstýringarfærsluna undir **Eining - Viðskiptakröfur** \> **Skjöl** \> **Reikningur með frjálsum texta**.

5. Stækkaðu **Eining - Viðskiptakröfur** \> **Skjöl** \> **Reikningur með frjálsum texta**, veldu færsluna **Upprunalegt** og fylgdu síðan þessum skrefum:

    1. Veldu og haltu niðri færslunni (eða hægrismelltu á hana) og veldu síðan **Hnekkja**.
    2. Veldu örvarhnappinn hægra megin við reitinn **Heiti áfangastaðar**.
    3. Á síðunni **Nefndur áfangastaður fyrir rafræna skýrslugerð**, á aðgerðasvæðinu, skal velja **Nýr**.
    4. Í reitinn **Heiti** skal færa inn **Áfangastaður US-001**.
    5. Í flýtiflipanum **Viðtökustaður skráar** skal [skilgreina](er-destination-type-print.md) áfangastað **Prentara** fyrir **Skýrsluhlutann**.
    6. Lokaðu síðunni **Nefndur áfangastaður fyrir rafræna skýrslugerð**.
    7. Á síðunni **Uppsetning á prentstýringu**, í reitnum **Heiti áfangastaðar**, skal velja **Áfangastaður US-001** fyrir nefndan áfangastað.

    ![Að skilgreina nefndan áfangastað rafrænnar skýrslugerðar fyrir valið snið rafrænnar skýrslugerðar og úthluta honum á skilgreinda færslu prentstýringar á uppsetningarsíðu prentstýringar](./media/er-named-destinations-02.gif)

    Þú hefur nú skilgreint **Áfangastaður US-001** fyrir nefndan áfangastað rafrænnar skýrslugerðar fyrir sniðið **Reikningur með frjálsum texta (Excel)** og úthlutað honum á **Upprunalegu** prentstýringarfærsluna undir **Eining - Viðskiptakröfur** \> **Lykill - US-001** \> **Reikningur með frjálsum texta**.

Nú, þegar unnið er úr reikningi með frjálsum texta, er rafræna skýrslugerðarsniðið **Reikningur með frjálsum texta (Excel)** keyrt og eitt af eftirfarandi tilvikum gerist:

- Ef reikningur með frjálsum texta er fyrir viðskiptavin annan en US-001 er myndað skjal sent í tölvupósti.
- Ef reikningur með frjálsum texta er fyrir viðskiptavin US-001 er myndað skjal prentað.

> [!NOTE]
> Þegar nefndur viðtökustaður hefur ekki verið skilgreindur fyrir færslu prentstýringar sem er unnið úr á keyrslutíma eru sjálfgefnir viðtökustaðir rafrænnar skýrslugerðar notaðir ef þeir eru í boði fyrir rafræna skýrslugerðarsniðið sem er í gangi.

> [!IMPORTANT]
> Á síðunni **Viðtökustaður rafrænnar skýrslugerðar** (**Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Viðtökustaður rafrænnar skýrslugerðar**), ef þú valdir snið rafrænnar skýrslugerðar sem a.m.k. einn nefndur viðtökustaður var skilgreindur fyrir færðu tilkynningu um að nefndir viðtökustaðir séu til staðar.
>
> ![Tilkynning um tilvist skilgreindra nefndra viðtökustaða fyrir valið snið rafrænnar skýrslugerðar á síðu viðtökustaðar rafrænnar skýrslugerðar](./media/er-named-destinations-03.png)
>
> Ef þú eyðir sjálfgefnum viðtökustað er öllum nefndum viðtökustöðum einnig eytt. Ef þessir nefndu viðtökustaðir voru valdir fyrir færslur prentstýringar er hætt við val á þessum nefndu viðtökustöðum.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Afrita fyrirliggjandi viðtökustað rafrænnar skýrslugerðar sem nýjan uppgefinn viðtökustað

Þegar sjálfgefið nefndur viðtökustaður rafrænnar skýrslugerðar er í boði fyrir snið rafrænnar skýrslugerðar er hægt að nota hann sem sniðmát fyrir nýja viðtökustaðir rafrænnar skýrslugerðar. Til að búa til nýjan viðtökustað rafrænnar skýrslugerðar sem byggir á sjálfgefnum viðtökustað skal velja **Afrita úr sjálfgefnu** á síðunni **Nefndur áfangastaður fyrir rafræna skýrslugerð**. Nýi áfangastaðurinn er nefndur **Sjálfgefið**. Þú getur endurtekið þetta skref eins oft og þörf krefur.

Þú getur valið fyrirliggjandi nefndan áfangastað sem sniðmát fyrir nýjan nefndan áfangastað. Til að búa til nýjan uppgefinn viðtökustað rafrænnar skýrslugerðar sem byggir á völdum uppgefnum viðtökustað skal velja **Afrita** á síðunni **Nefndur áfangastaður fyrir rafræna skýrslugerð**. Nýi áfangastaðurinn ber sama heiti og valinn nefndur áfangastaður, en viðskeytinu „Afrita“ er bætt við. Þú getur endurtekið þetta skref eins oft og þörf krefur.

## <a name="security-considerations"></a>Öryggisatriði

Þú getur aðeins sett upp nefnda áfangastaði rafrænnar skýrslugerðar á síðunni **Uppsetning á prentstýringu** ef þú hefur [heimild](../sysadmin/role-based-security.md#permissions) til að framkvæma þetta verk. Hægt er að veita þér heimild ef þú færð **Skilgreina viðtökustað rafræns skýrslugerðarsniðs** [aðgangsheimildina](../sysadmin/role-based-security.md#duties) úthlutaða á eitt af [öryggishlutverkum](../sysadmin/role-based-security.md#security-roles) þínum. Frekari upplýsingar er að finna í [Öryggisatriði](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Áfangastaðir fyrir rafræna skýrslugerð](electronic-reporting-destinations.md)

[Breytingar á API rafræns skýrslugerðarramma fyrir Application update 10.0.17](er-apis-app10-0-17.md)

[Breytingar á API rafræns skýrslugerðarramma fyrir Application update 10.0.21](er-apis-app10-0-21.md)

[Breyta kóða til að gera notendum kleift að skilgreina og nota nefnda áfangastaði rafrænnar skýrslugerðar](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
