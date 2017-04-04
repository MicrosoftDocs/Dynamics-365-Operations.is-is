---
title: "Stjórnun skilgreiningar á lífsferli Rafrænnar skýrslugerðar."
description: "Þetta efnisatriði lýsir því hvernig stjórna lifecycle fyrir Rafræna skýrslugerð skilgreiningar (ER) fyrir Microsoft Dynamics 365 fyrir lausn Aðgerðir."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Stjórnun skilgreiningar á lífsferli Rafrænnar skýrslugerðar.

Þetta efnisatriði lýsir því hvernig stjórna lifecycle fyrir Rafræna skýrslugerð skilgreiningar (ER) fyrir Microsoft Dynamics 365 fyrir lausn Aðgerðir.

<a name="overview"></a>Yfirlit
--------

Rafræn skýrslugerð (ER) er kerfi til að styðja lögboðin og landsértæk rafræn skjöl í Microsoft Dynamics 365 for Operations. Almennt hefur ER möguleikann á að framkvæma eftirfarandi verkefni fyrir stakt rafrænt skjal. Nánari upplýsingar, sjá [Rafræna skýrslugerð yfirlit](general-electronic-reporting.md).

-   Að hanna sniðmát fyrir rafrænt skjal:
    -   Auðkenna áskilinn uppruna gagna sem má setja fram í þessu fylgiskjali:
        -   Undirliggjandi Dynamics 365 fyrir Aðgerðir, eins og gagnatöflur gagnaeiningar og klasar.
        -   Ferli tiltekin eiginleika, eins og framkvæmd dagsetningu og tíma og tímabelti.
        -   Notandi inntaksfæribreyturnar, tilgreind notandinn á keyrslutíma.
    -   Skilgreina þarf nauðsynlegar einingar skjals sem og grannfræði þess til að tilgreina snið endanlegs skjals.
    -   Skilgreina þarf æskilegt flæði gagna frá völdum gagnagjafa til skilgreindra eininga skjals (í gegnum tengingar gagnagjafa við sniðsþætti skjals) og tilgreina rök vinnslustjórnunar.
-   Gera sniðmát tiltækt þannig að hægt er að nota það í öðrum tilvikum Dynamics 365 for Operations
    -   Umbreyta sniðmáti skjals sem var stofnað í Dynamics 365 for Operations yfir í ER skilgreiningu og flytja afbrigði úr núverandi tilviki Dynamics 365 for Operations sem xml-pakka sem hægt er að geyma annaðhvort staðbundið eða í LCS.
    -   Umbreyta skilgreiningu ER í sniðmát skjals í Dynamics 365 for Operations.
    -   Flytja inn xml-pakka sem geymdur er annað hvort staðbundið eða í LCS yfir í gildandi tilvik Dynamics 365 for Operations.
-   Sérsníða sniðmát rafræna skjalsins:
    -   Flytja sniðmát úr LCS yfir í núverandi tilvik Dynamics 365 for Operations sem ER-skilgreiningu.
    -   Hanna sérsniðna útgáfu ER skilgreiningar og halda tilvísun í grunnútgáfu hennar.
-   Samþætta sniðmát við tiltekið viðskiptaferli, þannig að það sé tiltækt í Dynamics 365 for Operations:
    -   Skilgreina stillingar í þannig að Dynamics 365 for Operations hefur að nota ER skilgreiningu með því að vísa í þá skilgreiningu í færibreytu sem er í tengslum við vinnslu. Til dæmis vísað ER skilgreiningu í tiltekna Lykla lánardrottna greiðslumáta til að mynda skilaboð úr rafræna greiðslu fyrir úrvinnslu reikninga.
-   Nota sniðmát í tilteknu viðskiptaferli:
    -   Keyra skilgreiningu ER í viðskiptaferli. Til dæmis til að mynda skilaboð úr rafræna greiðslu fyrir úrvinnslu reikninga þegar greiðslumáti sem vísar í skilgreiningu ER er valinn.

## <a name="concepts"></a>Hugtök
Eftirfarandi hlutverk og aðgerðir tengdar tengjast lifecycle ER skilgreiningu.

| Hlutverk                                       | Verkþættir                                                      | lýsing                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar | Stofna og stjórna íhlutum ER (líkön og snið).           | Business einstakling sem ER léni – tiltekin gagnalíkön, hannar hannar þarf sniðmát fyrir rafræn skjöl og binds þær samkvæmt því.                                                                           |
| Þróunaraðili rafrænnar skýrslulausnar             | Stofnar og stjórnar vörpunum gagnalíkana.                          | Í Dynamics 365 fyrir Aðgerðir sérfræðings sem velur þarf Dynamics 365 fyrir gagnagjafa Aðgerðir og binds þær ER léni – tiltekin gagnalíkön.                                                                 |
| Yfirmaður bókhalds                      | Skilgreinir stillingar á ferlum sem vísa til ER gervinga. | Til dæmis inn **yfirmaður Bókhalds** hlutverk sem leyfir stillingum ER skilgreining sem nota á í tiltekna Lykla lánardrottna greiðslumáta til að mynda skilaboð úr rafræna greiðslu fyrir úrvinnslu reikninga. |
| Starfsmaður viðskiptaskuldagreiðslna            | Notar ER gervinga í tilteknu viðskiptaferli.                | Til dæmis inn **viðskiptaskuldagreiðslna** hlutverk sem leyfir rafrænar greiðslur skilaboð að vera myndað fyrir úrvinnslu reikninga, byggðan á sniði ER sem er skilgreint fyrir tiltekinn greiðslumáta.           |

## <a name="er-configuration-development-lifecycle"></a>Þróunarlífsferill ER skilgreiningar.
Mælt er með að hanna ER skilgreiningar í þróunarumhverfi sem aðskilið tilvik af Dynamics 365 for Operations fyrir eftirfarandi ER málefni:

-   Notendur í hlutverkum annaðhvort **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar ** geta breytt stillingum og keyrt þær vegna prófunar. Það getur valdið köllun eftir aðferðum flokka og töflum sem geta hugsanlega verið skaðleg fyrir viðskiptagögn og árangur af notkun Dynamics 365 for Operations tilviks.
-   Köllun eftir aðferðum flokka og tafla sem ER gagnagjafa fyrir ER skilgreiningar eru ekki takmarkaðar af Dynamics 365 for Operations aðgangsstað og skráðu efni fyrirtækis. Því geta notendur sem eru í hlutverkum **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar ** fengið aðgang að viðkvæmum gögnum fyrirtækis.

Hægt er að hlaða upp ER skilgreiningar sem eru hannaðar í þróunarumhverfinu á prófunarumhverfi fyrir skilgreiningu mat (samþættingu viðeigandi vinnslu, réttmæti niðurstöður og afköst) og gæðatrygging eins og réttmæti hlutverk knúin aðgangsheimildir og aðskilnað á skyldum. Hægt er að nota skipti á skilgreiningu rafrænum ER að virkja aðgerðir í þessum tilgangi. Loks staðfest afbrigði ER hægt að hlaða inn á LCS, þar sem hægt að deila þeim með subscribers þjónustu, eða í framleiðsluumhverfið til innri nota eins og sýnt í eftirfarandi dæmi. ![ER lifecycle skilgreiningu](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Sjá einnig
--------

[Yfirlit yfir Rafræna skýrslugerð](general-electronic-reporting.md)


