---
title: Stofna forskilgreind afurðarafbrigði
description: Þetta ferli fer í gegnum stofnun afurðarafbrigða fyrir afurðarsniðmát með samsetningum fyrir afurðavíddir.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d3a4ae8efd438e01c263af1c0a1746d9484e491
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103099"
---
# <a name="predefined-product-variants"></a>Fyrirframskilgreind afurðarafbrigði

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Sýnidæmi: Stofna fyrirframskilgreind afurðarafbrigði

Þetta sýnidæmi sýnir hvernig á að stofna afurðarafbrigði fyrir afurðarsniðmát með því að nota samsetningar af afurðarafbrigðum.

### <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Til að fylgja þessari atburðarás með gögnunum sem mælt er með hér, verður þú að hafa sýnigögn sett upp og þú verður að velja lögaðilann *USMF*.

### <a name="step-1-create-a-product-master"></a>Skref 1: Stofna afurðarsniðmát

Til að stofna afurðarsniðmát

1. Fara í **Upplýsingastjórnun afurða > Afurðir > Afurðarsniðmát**.
1. Veljið **Nýtt**.
1. Ef reiturinn **Afurðarnúmer** sýnir ekki númer nú þegar skal færa inn gildi. Þetta er aðeins nauðsynlegt ef engin númeraröð hefur verið sett upp fyrir þennan reit.
1. Færið inn heiti í reitinn **Afurðarheiti**.
1. Í reitinn **Afurðavíddaflokkur** skal velja afurðavíddaflokkinn *SizeCol* (stærð og litur).
1. Veljið **Í lagi** til að stofna og opna nýtt afurðarsniðmát.

### <a name="step-2-add-product-dimensions"></a>Skref 2: Bæta við afurðarvíddum

Þetta dæmi sýnir hvernig á að færa inn afurðarvíddir handvirkt. Einnig er hægt að velja stærð, lit eða stílflokk sem inniheldur afurðarvíddargildi sem á að nota.

Til að bæta við afurðarvíddir

1. Með nýja afurðarsniðmátið enn opið skal velja **Afurðarvíddir** á aðgerðasvæðinu.
1. Opnið flipann **Stærð** og veljið **Ný** á tækjastikunni til að bæta línu við hnitanetið. Gerið eftirfarandi stillingar fyrir nýju línuna:
    - **Stærð:** Veljið stærðargildi.
    - **Heiti:** Færið inn heiti fyrir stærðina.
1. Veljið **Ný** á tækjastikunni og bætið annarri stærð við hnitanetið með nýrri **Stærð** og **Heiti**.
1. Opnið flipann **Litir** og veljið **Nýr** á tækjastikunni til að bæta línu við hnitanetið. Gerið eftirfarandi stillingar fyrir nýju línuna:
    - **Litur:** Veljið litargildi.
    - **Heiti:** Færið inn heiti fyrir litinn.
1. Veljið **Nýr** á tækjastikunni og bætið öðrum lit við hnitanetið með nýjum **Lit** og **Heiti**.
1. Veljið **Vista**.
1. Lokið síðunni til að fara aftur á nýja afurðarsniðmátið.

### <a name="step-3-generate-product-variants"></a>Skref 3: Búa til afurðarafbrigði

> [!NOTE]
> Þessi hluti lýsir því hvernig búa á til afurðarafbrigði þegar eiginleikinn *Endurbætur á tillögusíðu afbrigðis* er ekki virkur. Frekari upplýsingar um hvernig á að búa til afurðarafbrigði þegar þessi eiginleiki er í boði er að finna í næsta hluta.

Til að stofna afurðarafbrigði

1. Með nýja afurðarsniðmátið enn opið skal velja **Afurðarafbrigði** á aðgerðasvæðinu.
1. Veljið **Tillögur um afbrigði** á aðgerðasvæðinu.
1. Kerfið býr til lista með öllum mögulegum samsetningum stærða og lita sem þú skilgreindir fyrir afurðina. Veljið **Veljið allt** á tækjastikunni.
    - Í þessu dæmi skal velja öll möguleg afbrigði. Ef eingöngu á að nota undirsafn af mögulegum samsetningum afurðarvídda skal velja áskildu gátreitina eftir því sem þörf krefur.  
1. Velja **Stofna**.
1. Veljið **Vista**.

## <a name="improved-variant-suggestions"></a>Bættar tillögur um afbrigði

Eiginleikinn *Endurbætur á tillögusíðu afbrigðis* bætir síðuna **Tillögur um afbrigði** til að takast á við vandamál varðandi afköst og notagildi fyrir fyrirtæki sem eru með mikinn fjölda af samsetningum á afurðarvíddum. Bætt ferli til að velja afurðarvíddargildin þar sem á að búa til tillögur um afbrigði gerir það fljótlegra og auðveldara að bera kennsl á og gefa út viðeigandi safn af afurðarafbrigðum.

Eftirfarandi endurbótum er bætt við af þessum eiginleika:

- **Frestun á myndun afurðartillagna:** Síðan **Tillögur um afbrigði** sýnir ekki lengur tillögur þegar hún er opnuð í fyrsta skipti. Þess í stað þarf sérstaklega að velja hvaða gildi þarf og velja svo hnappinn **Leggðu til** til að mynda samsetningarnar. Þetta gerir ferlið sýnilegra og gagnvirkara.
- **Val víddargilda:** Þegar mörg víddargildi eru til staðar vill notandi yfirleitt búa til tillögur að afbrigðum sem taka aðeins nokkrar þeirra til greina (t.d. þegar nýir litir eða stílbrigði eru tekin í notkun). Með endurbættri hönnun er hægt að velja víddargildin fyrir það sem búa á tillögur að afurðarafbrigðum fyrir. Þetta eykur vægi þeirra afbrigða sem stungið er upp á og bætir bæði afköst kerfis og skilvirkni notanda.

### <a name="turn-the-variant-suggestions-page-improvements-feature-on-or-off"></a>Kveiktu eða slökktu á eiginleikanum fyrir endurbætur á afbrigðistillögum

Frá og með Supply Chain Management útgáfu 10.0.25 er sjálfgefið kveikt á þessum eiginleika. Stjórnendur geta kveikt eða slökkt á þessari virkni með því að leita að *Endurbætur á tillögum til afbrigða* eiginleiki í [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

### <a name="work-with-the-improved-variant-suggestions"></a>Unnið með endurbætur á tillögum afbrigðis

Til að búa til tillögur um afurðarafbrigði þegar kveikt er á eiginleikanum *Endurbætur á tillögusíðu afbrigðis*:

1. Opnið eða búið til afurðarsniðmát og bætið nauðsynlegum afurðarvíddum við það eins og lýst er í hlutanum hér á undan.
1. Með afurðarsniðmátið opið skal velja **Afurðarafbrigði** á aðgerðasvæðinu.
1. Veljið **Tillögur um afbrigði** á aðgerðasvæðinu.
1. Veljið gildin sem ætlunin er að nota fyrir hverja vídd fyrir sig.
1. Á efri tækjastikunni skal velja **Leggja til**.
1. Kerfið býr til lista með öllum mögulegum samsetningum stærða og lita sem voru valdar. Í flýtiflipanum **Afbrigði sem stungið er upp á** skal velja gátreitinn fyrir hverja samsetningu afurðarvíddar sem ætlunin er að nota eða velja **Velja allar** á tækjastikunni til að velja þær allar.  
1. Veljið **Búa til** til að bæta afbrigðunum við núverandi afurðarsniðmát.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
