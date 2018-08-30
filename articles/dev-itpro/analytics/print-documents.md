---
title: Skjalaprentun
description: "Í Microsoft Dynamics 365 for Finance and Operations er hægt að prenta skjöl með því að nota annaðhvort staðbundinn prentara eða nettengd tæki. Þessi grein gefur yfirlit yfir hvernig skjöl eru prentuð."
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5d52568ce49b85f6215ed2835a95e2e016c9c879
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="document-printing"></a>Skjalaprentun

[!include [banner](../includes/banner.md)]

Í Microsoft Dynamics 365 for Finance and Operations er hægt að prenta skjöl með því að nota annaðhvort staðbundinn prentara eða nettengd tæki. Þessi grein gefur yfirlit yfir hvernig skjöl eru prentuð.

<a name="printing-overview"></a>Yfirlit prentunar
-----------------

Microsoft Dynamics 365 for Finance and Operations veitir samþættar þjónustur og biðlaraforrit sem auðvelda að búa til, geyma og dreifa skjölum sem styðja viðskiptastarfsemi. Í Finance and Operations er hægt að prenta skjöl með því að nota annaðhvort staðbundinn prentara eða nettengt tæki. Að auki er hægt að flytja út síður og skýrslur Finance and Operations beint frá viðskiptavini, sem PDF-skrár eða Microsoft Office-skjöl. Að lokum gerir úthlutað vinnuálag þér kleift að prenta viðskiptaskjöl beint úr fartæki með því að nota nettilföng. Þótt prentskilyrði geta verið breytileg, þurfa allar atvinnugreinar yfirleitt að búa til afrit af viðskiptaskjölum með því að nota Finance and Operations. Prentun skjala á nettækjum frá hýstum forritum hefur í för með sér einstakt sett af áskorunum. Hér eru nokkur dæmi:

-   Prentrekill er hugsanlega ekki tiltækur á tæki notanda.
-   Tæki notanda kann að vera ótengt fyrirtækjanetinu.

Með því að nota sérstakan hýsil og fylgja nokkrum einföldum skrefum getur kerfisstjóri stillt uppsetningar þannig að notendur geti prentað beint úr viðskiptaforritum á nettækjum.

### <a name="printing-scenarios-in-finance-and-operations-applications"></a>Prentaðstæður í forritum fyrir Finance and Operations

Eftirfarandi tafla lýsir þremur helstu prentaðstæðunum í forritum fyrir Finance and Operations.

| Aðstæður                        | Markmið                                                      | Lausn                                                                                                            |
|---------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 1. Prenta það sem sést        | Prenta það sem er sýnt í vafranum.             | „Prentvæn“ útgáfa af vefsíðu er búin til fyrir vafrann.                                             |
| 2. Gagnvirk prentun         | Prenta nákvæmnisskjal á staðbundnu tengdu tæki. | Hægt er að flytja út PDF-útgáfa af skýrslunni og hlaðið henni niður í vafrann.                                          |
| 3. Prenta á nettæki | Senda nákvæmnisskjal á lén prenttækis.     | Nákvæmnisskjal er sent á biðlaraforrit sem keyrir á þjóni sem er hýstur á léni viðskiptavinar. |

Vegna þess að lausnin er breytileg, er háð aðstæðum, veita forrit Finance and Operations innbyggðar þjónustur og verkfæri til að hjálpa notendum að ná markmiðum sínum:

-   **Aðstæður 1** er studd af myndþýðingu vafrans á HTML5-biðlara.
-   **Aðstæður 2** notar biðlaraforrit og þjónustur Microsoft Office 365.
-   **Aðstæður 3** krefst stuðnings frá biðlaraforritum og þjónustum sem eru hýstar í Microsoft Azure.

Til viðbótar við verkvanginn sem er notaður á Azure-áskriftina, veita forrit Finance and Operations viðskiptavinum samþætt Azure-forrit frá fyrsta aðila sem auðveldar þeim að nota á lénhýst tæki til að prenta skjöl.

## <a name="service-overview"></a>Þjónustuyfirlit
Á meðan skjöl sem eru búin til af hýstum forritum bíða eftir að vera prentuð á nettengdu tæki, eru þau geymd í Azure blob-geymslu. [Leiðarmiðlari skjals](install-document-routing-agent.md) notar Azure sannvottun til að koma á öruggri rás til Azure-þjónustunnar. **Framkvæmdaröð**

1.  Skýrslan er búin til af Microsoft SQL Server Reporting Services (SSRS) og er geymd í Azure blob-geymslu. Viðhengdar prentarastillingar eru geymdar með skjalinu.
2.  Leiðarmiðlari skjals spyr brautarröð Azure Service um virk verk.
3.  Skjalinu er hlaðið niður með Leiðarmiðlara skjals og spólað á netprentarann.

Biðlaramiðuð lausnin leyfir viðskiptavinum að stjórna umfangi prentþarfa. Viðskiptavinir sem eru með mikið magn til prentunar geta sett upp marga Leiðarmiðlara skjals til að auka fjölda samhliða prentaðgerða. Að öðrum kosti þurfa sumir viðskiptavinir mjög fáar uppsetningar á Leiðarmiðlara skjals til að takast á við væntanlegar prentþarfir.

### <a name="service-components-for-network-printing"></a>Þjónustuíhlutir fyrir netprentun

Eftirfarandi skýringarmynd sýnir grunníhluti sem hjálpa til við að styðja netprentunaraðgerðir. [![þjónustuíhlutir-fyrir-netprentun\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png) Athugaðu að hægt er að skrá einn prentara með mörgum Leiðarmiðlurum skjals. Til að leysa kjörstillingar prentara notar hýst þjónusta netslóðina sem ber kennsl á hvern prentara fyrir sig. Þar af leiðandi, jafnvel þegar prentari er skráður af mörgum biðlurum, birtist hann sem eitt val á lista yfir prentara sem eru í boði í forritum Finance and Operations.




