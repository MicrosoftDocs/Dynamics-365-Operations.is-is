---
title: Yfirlit skjalaprentunar
description: Hægt er að prenta skjöl með því að nota annaðhvort staðbundinn prentara eða nettengt tæki. Þessi grein gefur yfirlit yfir hvernig skjöl eru prentuð.
author: RichdiMSFT
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom:
- "69161"
- intro-internal
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5a0d26836043ea225b9a6d3e62980ada2dc49b0a01a6dacec739b50f28e17bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728239"
---
# <a name="document-printing-overview"></a>Yfirlit skjalaprentunar

[!include [banner](../includes/banner.md)]

Hægt er að prenta skjöl með því að nota annaðhvort staðbundinn prentara eða nettengt tæki. Þessi grein gefur yfirlit yfir hvernig skjöl eru prentuð.

## <a name="printing-overview"></a>Yfirlit prentunar

Forritið veitir samþættar þjónustur og biðlaraforrit sem auðvelda að búa til, geyma og dreifa skjölum sem styðja viðskiptastarfsemi. Hægt er að prenta skjöl með því að nota annaðhvort staðbundinn prentara eða nettengt tæki. Að auki er hægt að flytja út síður og skýrslur beint frá viðskiptavini, sem PDF-skrár eða Microsoft Office skjöl. Að lokum gerir úthlutað vinnuálag þér kleift að prenta viðskiptaskjöl beint úr fartæki með því að nota nettilföng. Þótt prentskilyrði geta verið breytileg, þurfa allar atvinnugreinar yfirleitt að búa til afrit af viðskiptaskjölum með því að nota forritið. Prentun skjala á nettækjum frá hýstum forritum hefur í för með sér einstakt sett af áskorunum. Hér eru nokkur dæmi:

- Prentrekill er hugsanlega ekki tiltækur á tæki notanda.
- Tæki notanda kann að vera ótengt fyrirtækjanetinu.

Með því að nota sérstakan hýsil og fylgja nokkrum einföldum skrefum getur kerfisstjóri stillt uppsetningar þannig að notendur geti prentað beint úr viðskiptaforritum á nettækjum.

### <a name="application-printing-scenarios"></a>Atburðarprentun atburðarása 

Eftirfarandi tafla lýsir þremur aðalprentmyndum.

| Aðstæður                        | Markmið                                                      | Lausn |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Prenta það sem sést        | Prenta það sem er sýnt í vafranum.             | „Prentvæn“ útgáfa af vefsíðu er búin til fyrir vafrann. |
| 2. Gagnvirk prentun         | Prenta nákvæmnisskjal á staðbundnu tengdu tæki. | Hægt er að flytja út PDF-útgáfa af skýrslunni og hlaðið henni niður í vafrann. |
| 3. Prenta á nettæki | Senda nákvæmnisskjal á lén prenttækis.     | Nákvæmnisskjal er sent á biðlaraforrit sem keyrir á þjóni sem er hýstur á léni viðskiptavinar. |

Vegna þess að lausnin er breytileg, er háð aðstæðum, veita forrit innbyggðar þjónustur og verkfæri til að hjálpa notendum að ná markmiðum sínum:

- **Aðstæður 1** er studd af myndþýðingu vafrans á HTML5-biðlara.
- **Aðstæður 2** notar biðlaraforrit og þjónustu Microsoft 365.
- **Aðstæður 3** krefst stuðnings frá biðlaraforritum og þjónustum sem eru hýstar í Microsoft Azure.

Til viðbótar við verkvanginn sem er notaður á Azure-áskriftina, veita Finance and Operations forrit viðskiptavinum samþætt Azure-forrit frá fyrsta aðila sem auðveldar þeim að nota á lénhýst tæki til að prenta skjöl.

## <a name="service-overview"></a>Þjónustuyfirlit
Á meðan skjöl sem eru búin til af hýstum forritum bíða eftir að vera prentuð á nettengdu tæki, eru þau geymd í Azure blob-geymslu. [Setja upp eftirlitsbúnað skjalasendingar til að virkja nettengda prentun](install-document-routing-agent.md) notar Azure sannvottun til að koma á öruggri rás til Azure-þjónustunnar.

**Framkvæmdaröð**

1. Skýrslan er búin til af Microsoft SQL Server Reporting Services (SSRS) og er geymd í Azure blob-geymslu. Viðhengdar prentarastillingar eru geymdar með skjalinu.
2. Leiðarmiðlari skjals spyr brautarröð Azure Service um virk verk.
3. Skjalinu er hlaðið niður með Leiðarmiðlara skjals og spólað á netprentarann.

Biðlaramiðuð lausnin leyfir viðskiptavinum að stjórna umfangi prentþarfa. Viðskiptavinir sem eru með mikið magn til prentunar geta sett upp marga Leiðarmiðlara skjals til að auka fjölda samhliða prentaðgerða. Að öðrum kosti þurfa sumir viðskiptavinir mjög fáar uppsetningar á Leiðarmiðlara skjals til að takast á við væntanlegar prentþarfir.

### <a name="service-components-for-network-printing"></a>Þjónustuíhlutir fyrir netprentun

Eftirfarandi skýringarmynd sýnir grunníhluti sem hjálpa til við að styðja netprentunaraðgerðir.

[![þjónustu-hlutar-fyrir-net-prentun\_2016.](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Athugaðu að hægt er að skrá einn prentara með mörgum miðlum skjalasendingar. Til að leysa kjörstillingar prentara notar hýst þjónusta netslóðina sem ber kennsl á hvern prentara fyrir sig. Þar af leiðandi, jafnvel þegar prentari er skráður af mörgum biðlurum, birtist hann sem eitt val á lista yfir prentara sem eru í boði í forritunum.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]