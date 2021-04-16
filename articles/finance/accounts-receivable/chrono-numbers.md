---
title: Skjöl og fylgiskjöl númeruð eftir tímaröð
description: Þetta efnisatriði útskýrir hvernig á að setja upp og nota númer í tímaröð fyrir viðeigandi skjöl og tengd fylgiskjöl.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: fe533052b0e5b04a7d27b954ba644761c631d6d7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838862"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>Skjöl og fylgiskjöl númeruð eftir tímaröð

[!include [banner](../includes/banner.md)]


Í sumum löndum er lagaleg krafa um að númera skjöl og tengd fylgiskjöl í tímaröð. Tímaröðin verður að vera studd af tímabilum. Öll númer sem tilheyra fyrri tímabilum verða að vera minna en númerin sem tilheyra seinni tímabilum. Til að uppfylla þessa kröfu hefur númeravirkni í tímaröð verið innleidd. Þetta efnisatriði útskýrir hvernig á að skilgreina og nota númer í tímaröð fyrir viðeigandi skjöl og tengd fylgiskjöl.

## <a name="prerequisites"></a>Forkröfur

Á vinnusvæði eiginleikastjórnunar skal kveikja á eiginleikanum **Tölusetning í tímaröð**. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-chronological-numbering"></a>Skilgreina tölusetningu í tímaröð

Tölusetning í tímaröð hefur áhrif á eftirfarandi skjöl.

**Viðskiptakröfur**
- Reikningur viðskiptavina
- Fylgiskjal með reikningi viðskiptavinar
- Sölukreditnóta
- Fylgiskjal sölukreditnótu
- Textareikningur
- Fylgiskjal textareiknings
- Textakreditnóta
- Fylgiskjal textakreditnótu
- Fylgiseðill
- Fylgiskjal fylgiseðils
- Leiðréttingarskjal fyrir fylgiseðil
- Fylgiskjal vaxtanótu
- Fylgiskjal innheimtubréfs

**Viðskiptaskuldir**
- Fylgiskjal reiknings
- Fylgiskjal á kreditnótum
- Innhreyfingarskjal afurða

**Verkefnastjórnun**
- Reikningur
- Fylgiskjal reiknings
- Kreditnóta
- Fylgiskjal á kreditnótum 

### <a name="define-number-sequences"></a>Skilgreina númeraraðir

Til að skilgreina númeraraðir skal fara í **Fyrirtækisstjórnun** > **Númeraraðir** > **Númeraraðir**. Hægt er að skilgreina eins margar númeraraðir og þörf er á til að ná yfir tilheyrandi tímabil fyrir nauðsynleg skjöl. 

Tilgreinið fyrirtæki fyrir hverja númeraröð. Hlutar númeraraðanna verða að vera skilgreindir þannig að þeir bjóði upp á rétta tímaröð fyrir tímabil. Til dæmis geta heiti hlutanna innihaldið sérstakt forskeyti sem vísar í tiltekið tímabil.

![Uppsetning númeraraðar](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>Skilgreina númeraraðaflokka

Til að skilgreina númeraraðaflokka skal fara í **Viðskiptakröfur** > **Uppsetning** > **Færibreytur viðskiptakröfu**. Í flipanum **Númeraraðir** skal skilgreina eins marga númeraraðaflokka og þörf er á til að ná yfir tilheyrandi tímabil. 

Fyrir hvern flokk, í hlutanum **Tilvísun**, skal velja eina af studdu skjalatilvísununum og í reitnum **Númeraraðarkóði** skal vísa í númeraröð sem var áður búin til fyrir tilheyrandi tímabil.

![Uppsetning númeraraðaflokks](media/chrono-num-sequence-group.jpg)

Á svipaðan hátt skal skilgreina númeraraðaflokka í einingunum **Viðskiptaskuldir** og **Verkefnastjórnun og bókhald**.

### <a name="configure-number-sequence-groups-chronology"></a>Skilgreina tímaröð númeraraðaflokka

Til að skilgreina tímaröð númeraraðaflokka skal fara í **Fyrirtækisstjórnun** > **Númeraraðir** > **Númeraraðaflokkar í tímaröð**. Skilgreinið skilyrði númeraraðaflokks þegar hann tekur gildi.

![Uppsetning númera í tímaröð](media/chrono-num-sequence-group-period.jpg)

| Svæði            | lýsing                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Virkt  | Upphafsdagsetning þegar númeraraðaflokkur tekur gildi. |
| Lok gildistíma      | Lokadagsetning þegar númeraraðaflokkur gildir ekki lengur. Ef engin lokadagsetning á við skal velja **Aldrei**. |
| Númeraraðaflokkur | Númeraraðaflokkur sem verður notaður til að mynda skjalanúmer á tímabilinu. |
| Upprunalegur númeraraðarflokkur | Þessi kóði númeraraðaflokks er notaður fyrir frekari afmarkanir fyrir tilfelli þar sem skjöl eru þegar með tiltekinn *varanlegan* númeraraðaflokk úthlutaðan. Autt gildi er talið sérstakt gildi. Ef hunsa þarf fyrirfram úthlutaðan flokk skal nota valkostinn **Sjálfgefinn** fyrir þessa uppsetningu. |
| Sjálfgefinn | Ef kveikt er á þessu hunsar kerfið fyrirfram úthlutaðan númeraraðaflokk skjals og notar aðeins upphafs- og lokadagsetningar til að greina hvað á við. Ef slökkt er á þessu notar kerfið fullu samsetninguna **Virkt** + **Gildistími** + **Upprunalegur númeraraðaflokkur** fyrir val. |

## <a name="document-posting"></a>Bókun skjals
Þegar skjal er bókað er viðeigandi númeraraðaflokki úthlutað á skjalið byggt á bókunardagsetningu skjals og síðan notaður til að mynda skjalanúmer byggt á greindri númeraröð. Kerfið býður upp á skilaboð varðandi úthlutun númeraraðarflokks.

![Skjalnúmer](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> Í sumum löndum er þegar búið að innleiða ákveðna reglu fyrir númerasetningu skjala. Í slíku tilfelli mun regla tiltekins lands hnekkja eiginleikanum **Tölusetning í tímaröð**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
