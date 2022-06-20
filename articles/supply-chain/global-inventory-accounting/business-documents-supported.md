---
title: Viðskiptaskjöl studd af altæku birgðabókhaldi
description: Þessi grein sýnir viðskiptaskjölin sem eru studd af alþjóðlegu birgðabókhaldi. Þar er einnig að finna ítarlegt dæmi um skjöl innkaupapöntunar.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: dc88d095c039b22ac347db949f6b61d5a89dc4b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875424"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a>Viðskiptaskjöl studd af altæku birgðabókhaldi

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Eftir að innbót altæks birgðabókhalds er sett upp að fullu er það tilbúið til að vinna úr birgðatengdum skjölum sem eru færð inn í Microsoft Dynamics 365 Supply Chain Management.

## <a name="supported-business-documents"></a>Studd viðskiptaskjöl

Til eru tvær gerðir viðskiptaskjala:

- **Skjöl sem eru með færslubók** – Þessi skjöl eru m.a. innhreyfingarskjal afurðar, innkaupareikningur, fylgiseðill og sölureikningsskjöl.
- **Skjöl sem eru ekki með færslubók** – Þessi skjöl fela í sér skjöl talningar, hreyfingar og leiðréttingar á birgðum.

Síðar í þessari grein verða innkaupapantanir notaðar sem dæmi til að sýna ferlið.

Í eftirfarandi töflu er listi yfir skjöl sem núverandi útgáfa styður.

| Skjalagerð      | Skjal        |
|--------------------|-----------------|
| Innkaupapöntun     | Innhreyfingarskjal afurða |
| Innkaupapöntun     | Reikningur         |
| Sölupöntun        | Fylgiseðill    |
| Sölupöntun        | Reikningur         |
| Birgðabækur | Hreyfing        |
| Birgðabækur | Leiðrétting      |
| Birgðabækur | Talning        |
| Birgðabækur | Millifærsla        |
| Millifærslupöntun     | Sending        |
| Millifærslupöntun     | Taka á móti         |

> [!IMPORTANT]
> Altækt birgðabókhald vinnur ósamstillt úr skjölunum sem færð eru inn í Supply Chain Management. Engin villuboð verða sýnd ef upp koma vandamál með skjöl.

## <a name="example-purchase-order"></a>Dæmi: Innkaupapöntun

### <a name="product-receipt"></a>Innhreyfingarskjal afurða

Bókið innhreyfingarskjöl afurða eins og venjulega. Á síðunni **Allar innkaupapantanir** skal velja innkaupapöntun og síðan á aðgerðasvæðinu, í flipanum **Móttaka**, skal velja **Innhreyfingarskjal afurðar** til að opna síðuna **Færslubók innhreyfingarskjala afurða**. Tilvik aðgerðar og altækt birgðabókhaldstilvik eru búin til fyrir hverja línu. Því skal velja flipann **Línur** og velja síðan **Birgðir \> Tilvik og mælinga** til að opna síðuna **Tilvik og mælingar**.

Altækt birgðabókhald er bókhaldskerfi sem byggir á tilvikum og mælingum. Hnitanet mælingar á síðunni **Tilvik og mælingar** sýnir lista yfir mælingar. Hver mæling er með lista yfir víddir.

Fyrir hverja aðgerð eru tvær gerðir mælinga:

- **Aðgerðamælingar** – Þessar mælingar lýsa viðskiptaskjölum á almennan hátt. Ein mæling er afurðarmagnið með mælieiningunni sem er notuð í skjalinu. Einnig eru til mælingar sem hafa áhrif á birgðavirðið eins og heildarverð, afsláttur, afsláttarprósenta og línugjald.
- **Mælingar bókhaldstilfangs** – Þessar mælingar vinna út frá birgðaskráningunni. Þær lýsa áhrifum skjalsins á birgðir í mælieiningu birgða. Ef margar birgðaskráningar eru til staðar eru margar línur af mælingum á bókhaldstilfangi.

Víddirnar eru skipulagðar með eftirfarandi hætti:

- **Tvískipting** – Tvískipting lýsir aðilunum sem taka þátt í fjárhagstilvikinu. Fyrir ytri viðskiptaskjöl lýsa aðalvíddirnar lögaðilanum þar sem skjalið er fært inn á meðan tvískiptar víddir lýsa lánardrottini, viðskiptavini o.s.frv. Fyrir innri viðskiptaskjöl (t.d. flutningspantanir) lýsa tvískiptar víddir vöruhúsi mótaðila.
- **Gerð víddar** – Víddargerðir flokka víddirnar.
- **Vídd** – Heiti víddar.
- **Víddargildi** – Gildi víddar.

### <a name="global-inventory-accounting-event"></a>Altækt birgðabókhaldstilvik

Altækt birgðabókhald lítur á rekstrartilvik og mælingar sem inntak. Það gerir síðan viðeigandi bókhald fyrir hvern tengdan fjárhag sem byggir á meðfylgjandi gjaldmiðli og venju. Hægt er að velja **Altækt birgðabókhaldstilvik og mælingar** til að skoða altækt birgðabókhaldstilvik. Altækt birgðabókhaldstilvik fylgir sömu aðferðarfræðinni og rekstrartilvik, en það notar aðrar mælingar. Þrjár stærstu mælingargerðirnar eru: kostnaðarmagn afurðar, kostnaður afurðar og frávik.

Fjárhagslyklar undirbókar eru notaðir til að flokka mælingarnar enn frekar. Hugsanlega eru margar fjárhagsbækur. Þessar fjárhagsbækur tengjast lögaðilanum þar sem skjalið er fært inn. Hægt er að skoða tilvik og mælingar fyrir hverja fjárhagsbók með því að breyta gildinu í reitnum **Fjárhagur**.

### <a name="cost-element"></a>Kostnaðareining

Á grundvelli stefnu um kostnaðareiningu sem fylgir fjárhagsbókinni úthlutar kerfið kostnaðareiningu á hverja reiknaða mælingu rekstrartilviks sem hefur áhrif á birgðakostnaðinn. Þessar mælingar fela í sér heildarverð, afslátt, afsláttarprósentu og línugjald.

### <a name="measurement-line-details"></a>Upplýsingar um línu mælingar

Flipinn **Yfirlit** sýnir upplýsingar um meðfylgjandi stefnur. Víddir kostnaðarhlutar sýna kostnaðarhlutinn samkvæmt stefnu um kostnaðarhlut. Sérstakar auðkenningavíddir sýna rununúmerið ef ályktun kostnaðarflæðis er *Tiltekin – Runa*.

### <a name="purchase-invoice"></a>Innkaupareikningur

Bókið reikninginn eins og venjulega. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Færslubækur** skal síðan velja **Reikning** til að opna reikningabókina. Tilvik aðgerðar og altækt birgðabókhaldstilvik eru búin til fyrir hverja línu. Því skal velja flipann **Línur** og velja síðan **Birgðir \> Tilvik og mælinga** til að opna síðuna **Tilvik og mælingar**. Á síðunni **Tilvik og mælingar** má sjá sömu gerð mælingar. En vegna þess að síðan sýnir mismunandi hlutverk mælingar og breytilykills, verða áhrifin á aðilann (lögaðilann) mismunandi.

Veljið **Altækt birgðabókhaldstilvik og mælingar** til að skoða altækt birgðabókhaldstilvik. Birgðamagn og kostnaður renna nú úr lykli undirbókarinnar *Vörur mótteknar en ekki reikningsfærðar birgðir* og í lykil undirbókarinnar *Kostnaður keyptra vara*.
