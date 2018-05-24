---
title: "Stjórnun skilgreiningar á lífsferli Rafrænnar skýrslugerðar."
description: "Þetta efnisatriði lýsir því hvernig á að stjórna lífsferli skilgreininga rafrænnar skýrslugerðar (ER) fyrir Microsoft Dynamics 365 for Finance and Operations lausnina."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f3d6463ab07aaaf69a16aa0d59840cbe47427335
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Stjórnun líftíma skilgreiningar fyrir rafræna skýrslugerð

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að stjórna lífsferli skilgreininga rafrænnar skýrslugerðar (ER) fyrir Microsoft Dynamics 365 for Finance and Operations lausnina.

<a name="overview"></a>Yfirlit
--------

Rafræn skýrslugerð (ER) er kerfi til að styðja lögboðin og landsértæk rafræn skjöl í Microsoft Dynamics 365 for Finance and Operations. Almennt hefur ER möguleikann á að framkvæma eftirfarandi verkefni fyrir stakt rafrænt skjal. Frekari upplýsingar eru í [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md).

-   Að hanna sniðmát fyrir rafrænt skjal:
    -   Auðkenna áskilinn uppruna gagna sem má setja fram í þessu fylgiskjali:
        -   Undirliggjandi Finance and Operations-gögn, t.d. gagnatöflur, gagnaeiningar og flokkar.
        -   Ferlistengdir eiginleikar, t.d. dagsetning og tími keyrslu og tímabelti.
        -   Innsláttarfæribreytur notanda, tilgreindar af notanda á keyrslutíma.
    -   Skilgreina þarf nauðsynlegar einingar skjals sem og grannfræði þess til að tilgreina snið endanlegs skjals.
    -   Skilgreina þarf æskilegt flæði gagna frá völdum gagnagjafa til skilgreindra eininga skjals (í gegnum tengingar gagnagjafa við sniðsþætti skjals) og tilgreina rök vinnslustjórnunar.
-   Gera sniðmát tiltækt þannig að hægt sé að nota það í öðrum tilvikum Finance and Operations:
    -   Umbreyta sniðmáti skjals sem var stofnað í Finance and Operations í ER skilgreiningu og flytja skilgreininguna úr núverandi tilviki Finance and Operations sem XML-pakka sem hægt er að geyma annaðhvort staðbundið eða í LCS.
    -   Umbreyta skilgreiningu ER í sniðmát skjals í Finance and Operations.
    -   Flytja inn XML-pakka sem geymdur er annaðhvort staðbundið eða í LCS yfir í gildandi tilvik Finance and Operations.
-   Sérsníða sniðmát rafræna skjalsins:
    -   Flytja sniðmát úr LCS yfir í núverandi tilvik Finance and Operations sem ER-skilgreiningu.
    -   Hanna sérsniðna útgáfu ER skilgreiningar og halda tilvísun í grunnútgáfu hennar.
-   Samþætta sniðmát við tiltekið viðskiptaferli, þannig að það sé tiltækt í Finance and Operations:
    -   Skilgreina stillingar þannig að Finance and Operations byrjar að nota ER-skilgreiningu með því að vísa í þá skilgreiningu í færibreytu sem er í tengslum við vinnslu. Til dæmis vísa í skilgreiningu rafrænnar skýrslugerðar í tilteknum greiðslumáta fyrir viðskiptaskuldir til að mynda rafræn greiðsluskilaboð fyrir úrvinnslu reikninga.
-   Nota sniðmát í tilteknu viðskiptaferli:
    -   Keyra skilgreiningu rafrænnar skýrslugerðar í tilteknu viðskiptaferli. Til dæmis til að mynda skilaboð rafrænnar greiðslu fyrir úrvinnslu reikninga þegar greiðslumáti sem vísar til skilgreiningar rafrænnar skýrslugerðar er valinn.

## <a name="concepts"></a>Hugtök
Eftirfarandi hlutverk og tengdar aðgerðir tengjast lífsferli skilgreiningar rafrænnar skýrslugerðar.

| Hlutverk                                       | Verkþættir                                                      | lýsing                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar | Stofna og stjórna íhlutum ER (líkön og snið).           | Viðskiptaaðili sem hannar sértæk gagnalíkön rafrænnar skýrslugerðar fyrir tiltekin svið hannar áskilin sniðmát fyrir rafræn skjöl og tengir þau saman á viðeigandi hátt.                                                                           |
| Þróunaraðili rafrænnar skýrslulausnar             | Stofnar og stjórnar vörpunum gagnalíkana.                          | Finance and Operations sérfræðingur sem velur viðeigandi gagnagjafa Finance and Operations og tengir þá við sértæk gagnalíkön rafrænnar skýrslugerðar fyrir tiltekin svið.                                                                 |
| Yfirmaður bókhalds                      | Skilgreinir stillingar á ferlum sem vísa til ER gervinga. | Til dæmis hlutverkið **Yfirmaður bókhalds** sem leyfir að nota stillingar skilgreiningar rafrænnar skýrslugerðar fyrir tiltekinn greiðslumáta viðskiptaskulda til að geta búið til rafræn greiðsluskilaboð fyrir úrvinnslu reikninga. |
| Starfsmaður viðskiptaskuldagreiðslna            | Notar ER gervinga í tilteknu viðskiptaferli.                | Til dæmis hlutverk **Starfsmanns viðskiptaskuldagreiðslna** sem leyfir að mynda rafræn greiðsluskilaboð fyrir úrvinnslu reikninga, byggt á sniði rafrænnar skýrslugerðar sem er skilgreint fyrir tiltekinn greiðslumáta.           |

## <a name="er-configuration-development-lifecycle"></a>Þróunarlífsferill ER skilgreiningar.
Mælt er með að hanna ER skilgreiningar í þróunarumhverfi sem aðskilið tilvik af Finance and Operations fyrir eftirfarandi ER málefni:

-   Notendur í hlutverkum annaðhvort **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar** geta breytt stillingum og keyrt þær vegna prófunar. Þessar aðstæður geta valdið köllun eftir aðferðum flokka og töflum sem geta hugsanlega verið skaðleg fyrir viðskiptagögn og árangur af notkun Finance and Operations tilviks.
-   Köllun eftir aðferðum flokka og tafla sem ER gagnagjafa fyrir ER skilgreiningar er ekki takmörkuð af Finance and Operations aðgangsstöðum og skráðu efni fyrirtækis. Því geta notendur sem eru í hlutverkum **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar** fengið aðgang að viðkvæmum gögnum fyrirtækis.

Skilgreiningar rafrænar skýrslugerðar sem eru hannaðar í þróunarumhverfi má hlaða upp í prófunarumhverfi fyrir skilgreiningarmat (rétt samþætting vinnslu, nákvæmni niðurstaða og afköst) og gæðatryggingu, til dæmis réttmæti aðgangsheimilda sem eru knúin af hlutverkum, aðskilnaður á skyldum o.s.frv.). Hægt er að nota eiginleika til að skiptast á skilgreiningum rafrænnar skýrslugerðar í þessum tilgangi. Loks er hægt að hlaða upp sönnuðum skilgreiningum rafrænnar skýrslugerðar annaðhvort í LCS til að deila með áskrifendum þjónustu eða í framleiðsluumhverfi til innri notkunar, eins og sýnt er á eftirfarandi mynd. ![Lífsferill skilgreiningar rafrænnar skýrslugerðar](./media/ger-configuration-lifecycle.png)

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)




