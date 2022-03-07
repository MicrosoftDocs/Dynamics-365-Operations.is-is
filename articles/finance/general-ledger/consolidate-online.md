---
title: Sameiningar fjárhags á netinu
description: Í þessu efnisatriði er fjallað um sameiningu fjárhags á netinu í Fjárhag.
author: aprilolson
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: eca0d30903985126412e1ae0b8e3232c3e4700f4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351685"
---
# <a name="online-financial-consolidations"></a>Sameiningar fjárhags á netinu

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er fjallað um sameiningu fjárhags á netinu í Fjárhag. Áður en þú lest þetta efnisatriði skaltu fyrst lesa efnisatriðið [Yfirlit yfir sameiningar fjárhags og umreikning gjaldmiðils](financial-consolidations-currency-translation.md).

Eftir að þú hefur lokið uppsetningunni, slærðu inn upplýsingar um sameiningu á síðunni **Sameina [á netinu]**. Þegar því er lokið geturðu smellt á **Í lagi** eða **Runa** til að vinna úr sameiningunni.

## <a name="criteria"></a>Skilyrði
Á flipanum **Skilyrði** á síðunni **Sameina [á netinu]** skilgreinir þú reikningana, tímabilin og tegund af gögnum sem er verið að sameina.

![Flipinn Skilyrði.](./media/criteria-consolidate-online.png "Flipinn Skilyrði")

Hér er skýring á ýmsum reitum á þessum flipa:

- **Lýsing** - Sláðu inn nákvæma lýsingu á því tímabili sem þú ert að sameina.
- **Aðallykill** - Notaðu reitina í þessum kafla til að skilgreina helstu lykla sem verður unnið úr.

    - **Frá** og **Til** - Tilgreindu fjölda lykla sem á að vinna úr. Ef þú sleppir þessum reitum verða allir lyklar frá öllum fyrirtækjum fluttir til samstæðufyrirtækisins. Ef þú ert þar af leiðandi að sameina fjögur fyrirtæki og hvert fyrirtæki hefur annan bókhaldslykil verða allir lyklar frá öllum fjórum fyrirtækjum stofnaðir í samstæðufyrirtækinu.
    - **Nota samstæðulykil** - Ef þessi valkostur er stilltur á **Já** verður reiturinn **Velja samstæðulykil frá** tiltækur. Í þessum reit skaltu velja hvort allir lyklar skuli sameinaðir við samstæðulykilinn sem er stilltur á síðunni **Aðallykill** eða hvort þú vilt velja lykilinn úr einum af samstæðulyklaflokkunum.
    - **Samstæðulyklaflokkur** - Veldu flokkinn sem á að nota fyrir vörpun aðallykilsins fyrir sameininguna.

- **Samstæðutímabil** - Notaðu reitina í þessum kafla til að skilgreina samstæðutímabilið.

    - **Frá** og **Til** - Tilgreindu dagsetningarsvið fyrir samstæðuna. Ef þú sleppir þessum reitum verður samstæðan unnin fyrir öll tímabil sem eru skilgreind í fjárhagsdagatali fyrirtækis. Við mælum ekki með að þú sleppir þessum reitum.
    - **Hafa með raunverulegar upphæðir** - Stilltu þennan möguleika á **Já** til að sameina raungögnin þín.
    - **Hafa með upphæðir fjárhagsáætlunar** - Stilltu þennan möguleika á **Já** til að sameina gögn úr fjárhagsáætlunarskrá.
    - **Endurbyggja stöður í samstæðuferli** - Við mælum ekki með að þú stillir þennan möguleika á **Já**. Endurbyggðu stöður í staðinn sem aðskilda runuvinnslu.

- **Fjárhagsáætlunarlíkan** - Ef þú hefur valið að sameina fjárhagsáætlunargögn skaltu nota reitina í þessum kafla til að skilgreina fjárhagsáætlunarlíkönin.

    - **Frá** og **Til** - Tilgreindu líkanasviðið sem á að nota.
    - **Gengisgerð fjárhagsáætlunar** - Veldu gerð fyrir gengi fjárhagsáætlunar sem nota á fyrir umreikning gjaldmiðils á fjárhagsáætlunargögnum.

## <a name="financial-dimensions"></a>Fjárhagsvíddir
Á flipanum **Fjárhagsvíddir** skilgreinir þú víddirnar sem ætti að hafa með í samstæðufyrirtækinu. Til að velja vídd skaltu stilla reitinn **Lýsing** á **Vídd** og þá skilgreina röð víddarinnar í samstæðufyrirtækinu.

![Flipinn Fjárhagsvíddir.](./media/financial-dimensions-cons.png "Flipinn Fjárhagsvíddir")

Burtséð frá röðinni sem þú skilgreinir, þá verður **Aðallykill** alltaf fyrsti hlutinn.

## <a name="legal-entities"></a>Lögaðilar
Á flipanum **Lögaðila** skilgreinir þú fyrirtækin sem ætti að hafa með í fyrirtækjasamstæðunni. Þú skilgreinir einnig eignarhlutfall þessara fyrirtækja. Ef þú tilgreinir minna en 100 prósent eignarhald verður tilgreint hlutfall fært yfir á samstæðufyrirtækið. Fyrir allan mun í umreikningi er reiturinn **Lyklagerð fyrir umreikningsmun** notaður til að velja aðallykil frá uppsetningunni á síðunni **Lyklar fyrir sjálfvirkar færslur**.

![Flipinn Lögaðilar.](./media/legal-entities-cons.png "Flipinn Lögaðilar")

![Síðan Lyklar fyrir sjálfvirkar færslur.](./media/accounts-for-automatic-cons.png "Síðan Lyklar fyrir sjálfvirkar færslur")

## <a name="elimination"></a>Losun
Á flipanum **Losun** hefur þú þrjá valkosti fyrir úrvinnslu á losunum:

- Veldu losunarregluna og þá í reitnum **Valkostir tillagna** skaltu velja **Aðeins tillaga**. Þessi valkostur mun vinna úr losuninni meðan á samstæðuferlinu stendur, en hann mun ekki birta allt í einu skrefi. Þú getur bókað færslubókina seinna.
- Veldu losunarregluna og þá í reitnum **Valkostir tillagna** skaltu velja **Aðeins bóka**. Þessi valkostur mun vinna úr losuninni meðan á samstæðuferlinu stendur, og hann mun bóka allt í einu skrefi.
- Keyrðu losunartillögu aðskilið frá samstæðulykli með því að nota losunarfærslubókina.

![Flipinn Losun.](./media/elimination-cons-onl.png "Flipinn Losun")

Frekari upplýsingar um brotthvarf er að finna í [Losunarreglur](./elimination-rules.md).

## <a name="currency-translation"></a>Umreikningur gjaldmiðils
Á flipanum **Umreikningur gjaldmiðils** skilgreinir þú lögaðilann, lykilinn og gerð gengis og gengi. Þrír valkostir eru í boði í reitnum **Nota gengi frá**:

- **Dagsetning samstæðu** - Dagsetning samstæðunnar verður notuð til að fá gengið. Þetta gengi jafngildir stundargengi eða gengi við mánaðarlok. Þú munt sjá forskoðun á genginu, en þú getur ekki breytt því.
- **Færsludagsetning** - Dagsetning hverrar færslu verður notuð til að velja gengi. Þessi valkostur er oftast notaður fyrir eign og er oft nefnt sögulegt gengi. Þú getur ekki séð forskoðun á genginu vegna þess að það eru mörg gengi fyrir hinar ýmsu færslur á sviði lykils.
- **Notandaskilgreint gengi** - Eftir að þú hefur valið þennan valkost getur þú slegið inn það gengi sem þú vilt. Þessi valkostur getur verið gagnlegur fyrir meðalgengi eða ef þú sameinar gagnvart föstu gengi.

![Flipinn Umreikningur gjaldmiðils.](./media/currency-translation-cons-online.png "Flipinn Umreikningur gjaldmiðils")

## <a name="additional-resources"></a>Frekari upplýsingar

Nánari upplýsingar um samstæðuumreikning og umreikning gjaldmiðils er að finna í yfirefni þessa efnisatriðis, [Yfirlit yfir fjárhagssamstæður og umreikninga gjaldmiðils](./financial-consolidations-currency-translation.md).

Nánari upplýsingar um aðstæður þar sem þú gætir búið til samstæðureikningsskil er að finna í [Búa til samstæðureikningsskil](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]