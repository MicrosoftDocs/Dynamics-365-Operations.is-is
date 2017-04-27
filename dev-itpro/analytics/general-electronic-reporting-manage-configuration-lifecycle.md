---
title: "Stjórnun skilgreiningar á lífsferli Rafrænnar skýrslugerðar."
description: "Þetta efnisatriði lýsir hvernig á að stjórna lífsferli skilgreininga rafrænnar skýrslugerðar (ER) fyrir Microsoft Dynamics 365 for Operations-lausnina."
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

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir hvernig á að stjórna lífsferli skilgreininga rafrænnar skýrslugerðar (ER) fyrir Microsoft Dynamics 365 for Operations-lausnina.

<a name="overview"></a>Yfirlit
--------

Rafræn skýrslugerð (ER) er kerfi til að styðja lögboðin og landsértæk rafræn skjöl í Microsoft Dynamics 365 for Operations. Almennt hefur ER möguleikann á að framkvæma eftirfarandi verkefni fyrir stakt rafrænt skjal. Frekari upplýsingar eru í [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md).

-   Að hanna sniðmát fyrir rafrænt skjal:
    -   Auðkenna áskilinn uppruna gagna sem má setja fram í þessu fylgiskjali:
        -   Undirliggjandi Dynamics 365 for Operations-gögn, t.d. gagnatöflur, gagnaeiningar og flokkar.
        -   Ferlistengdir eiginleikar, t.d. dagsetning og tími keyrslu og tímabelti.
        -   Innsláttarfæribreytur notanda, tilgreindar af notanda á keyrslutíma.
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
    -   Skilgreina stillingar í þannig að Dynamics 365 for Operations hefur að nota ER skilgreiningu með því að vísa í þá skilgreiningu í færibreytu sem er í tengslum við vinnslu. Til dæmis vísa í skilgreiningu rafrænnar skýrslugerðar í tilteknum greiðslumáta fyrir viðskiptaskuldir til að mynda rafræn greiðsluskilaboð fyrir úrvinnslu reikninga.
-   Nota sniðmát í tilteknu viðskiptaferli:
    -   Keyra skilgreiningu rafrænnar skýrslugerðar í tilteknu viðskiptaferli. Til dæmis til að mynda skilaboð rafrænnar greiðslu fyrir úrvinnslu reikninga þegar greiðslumáti sem vísar til skilgreiningar rafrænnar skýrslugerðar er valinn.

## <a name="concepts"></a>Hugtök
Eftirfarandi hlutverk og tengdar aðgerðir tengjast lífsferli skilgreiningar rafrænnar skýrslugerðar.

| Hlutverk                                       | Verkþættir                                                      | lýsing                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar | Stofna og stjórna íhlutum ER (líkön og snið).           | Viðskiptaaðili sem hannar sértæk gagnalíkön rafrænnar skýrslugerðar fyrir tiltekin svið hannar áskilin sniðmát fyrir rafræn skjöl og tengir þau saman á viðeigandi hátt.                                                                           |
| Þróunaraðili rafrænnar skýrslulausnar             | Stofnar og stjórnar vörpunum gagnalíkana.                          | Er Dynamics 365 for Operations-sérfræðingur sem velur viðeigandi Dynamics 365 for Operations-gagnagjafa og tengir þá við sértæk gagnalíkön rafrænnar skýrslugerðar fyrir tiltekin svið.                                                                 |
| Yfirmaður bókhalds                      | Skilgreinir stillingar á ferlum sem vísa til ER gervinga. | Til dæmis hlutverkið **Yfirmaður bókhalds ** sem leyfir að nota stillingar skilgreiningar rafrænnar skýrslugerðar fyrir tiltekinn greiðslumáta viðskiptaskulda til að geta búið til rafræn greiðsluskilaboð fyrir úrvinnslu reikninga. |
| Starfsmaður viðskiptaskuldagreiðslna            | Notar ER gervinga í tilteknu viðskiptaferli.                | Til dæmis hlutverk **Starfsmanns viðskiptaskuldagreiðslna** sem leyfir að mynda rafræn greiðsluskilaboð fyrir úrvinnslu reikninga, byggt á sniði rafrænnar skýrslugerðar sem er skilgreint fyrir tiltekinn greiðslumáta.           |

## <a name="er-configuration-development-lifecycle"></a>Þróunarlífsferill ER skilgreiningar.
Mælt er með að hanna ER skilgreiningar í þróunarumhverfi sem aðskilið tilvik af Dynamics 365 for Operations fyrir eftirfarandi ER málefni:

-   Notendur í hlutverkum annaðhvort **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar ** geta breytt stillingum og keyrt þær vegna prófunar. Það getur valdið köllun eftir aðferðum flokka og töflum sem geta hugsanlega verið skaðleg fyrir viðskiptagögn og árangur af notkun Dynamics 365 for Operations tilviks.
-   Köllun eftir aðferðum flokka og tafla sem ER gagnagjafa fyrir ER skilgreiningar eru ekki takmarkaðar af Dynamics 365 for Operations aðgangsstað og skráðu efni fyrirtækis. Því geta notendur sem eru í hlutverkum **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar ** fengið aðgang að viðkvæmum gögnum fyrirtækis.

Skilgreiningar rafrænar skýrslugerðar sem eru hannaðar í þróunarumhverfi má hlaða upp í prófunarumhverfi fyrir skilgreiningarmat (rétt samþætting vinnslu, nákvæmni niðurstaða og afköst) og gæðatryggingu, til dæmis réttmæti aðgangsheimilda sem eru knúin af hlutverkum, aðskilnaður á skyldum o.s.frv.). Hægt er að nota eiginleika til að skiptast á skilgreiningum rafrænnar skýrslugerðar í þessum tilgangi. Loks er hægt að hlaða upp sönnuðum skilgreiningum rafrænnar skýrslugerðar annaðhvort í LCS til að deila með áskrifendum þjónustu eða í framleiðsluumhverfi til innri notkunar, eins og sýnt er á eftirfarandi mynd. ![Lífsferill skilgreiningar rafrænnar skýrslugerðar](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Sjá einnig
--------

[Yfirlit yfir Rafræna skýrslugerð](general-electronic-reporting.md)




