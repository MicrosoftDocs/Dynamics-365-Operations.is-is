---
title: Listi yfir birgðir á lager
description: Þetta efnisatriði lýsir því hvernig á að nota listasíðu lagerbirgða til að skoða upplýsingar um lagerbirgðir. Það sýnir nokkrar af þeim leiðum þar sem ýmsir síunar- og flokkunarvalkostir vinna saman og hvernig þessir valkostir geta stundum leitt til óvæntra niðurstaðna þegar þeir eru sameinaðir.
author: sherry-zheng
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem, InventOnHandItemListPage, WHSOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1e054c4010f730519532b67fe900573480ea2a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825988"
---
# <a name="inventory-on-hand-list"></a>Listi yfir birgðir á lager

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að nota síðuna **Lagerlisti** til að skoða upplýsingar um lagerbirgðir. Það sýnir nokkrar af þeim leiðum þar sem ýmsir síunar- og flokkunarvalkostir vinna saman og hvernig þessir valkostir geta stundum leitt til óvæntra niðurstaðna þegar þeir eru sameinaðir.

## <a name="query-your-on-hand-inventory"></a>Fyrirspurn send á lagerbirgðir

Til að skoða framboð á birgðum skal fara í **Birgðastjórnun \> Fyrirspurnir og skýrslur \> Lagerlisti**.

Síðan **Lagerlisti** er sjálfkrafa uppfærð þegar færslur eru gerðar í birgðum. Færslurnar kunna að vera áætlaðar, efnislegar eða fjárhagslegar.

Notið eftirfarandi verkfæri til að finna safn af afurðum sem leitað er að:

- Á aðgerðasvæðinu skal velja [**Víddir**](#dimensions) til að opna svarglugga þar sem hægt er að bæta við eða fjarlægja dálka sem eru sýndir í hnitanetinu **Á lager**.
- Á [**Síur** svæðinu](#filters-pane) skal færa inn gildi fyrir tiltekna reiti til að sýna aðeins færslur sem samsvara þessum gildum. Athugið að síur sem eru skilgreindar hér eiga við um upprunatöflur sem gæti seinna verið safnað saman, samkvæmt víddunum sem var valið að sýna. Upplýsingar um hvernig þessi hegðun getur haft áhrif á niðurstöðurnar er að finna í [dæmunum](#examples) seinna í þessu efnisatriði.
- Á svæðinu **Síur** skal velja **Nota** til að búa til listann yfir samsvarandi lagerbirgðir í hnitanetinu **Á lager**.
- Í hnitanetinu **Á lager** skal velja einhvern dálkahaus til að raða eða sía eftir gildum í þeim dálki. QuickFilter efst í hnitanetinu býður upp á fleiri síuvalkosti. Þessar síur eiga við um niðurstöðurnar, ekki upprunatöfluna. Upplýsingar um hvernig þessi hegðun getur haft áhrif á niðurstöðurnar er að finna í [dæmunum](#examples) seinna í þessu efnisatriði.

Fyrir hverja samsvarandi vöru býður hnitanetið **Á lager** upp á eftirfarandi dálka af birgðaupplýsingum.

| Dálkur | lýsing |
|---|---|
| Efnislegar birgðir | Efnislega magnið sem er tiltækt í birgðum. |
| Efnislegt magn frátekið | Heildarmagnið sem var tekið efnislega frá. |
| Efnislegt magn til ráðstöfunar | Tiltækt (ekki frátekið) magn sem er tiltækt í efnislegum birgðum.<p>**Efnislega tiltækt** er reiknaður reitur. Gildið jafngildir gildinu **Efnislegar birgðir** að frádregnu gildinu **Efnislega frátekið**.</p> |
| Efnislega til staðar í viðbótarvíddum | Tiltækt efnislegt magn fyrir allar víddirnar sem eru sýndar í hnitanetinu. |
| Samtals pantað | Heildarmagnið sem er tekið með í pöntunum á innleið eða sem er með jákvætt magn í ýmsum birgðabókum. |
| Í pöntun | Heildarmagnið sem er tekið með í pöntunum á útleið eða sem er með neikvætt magn í ýmsum birgðabókum. |
| Pantað frátekið | Heildarmagnið sem er frátekið fyrir pantaðar innhreyfingar. Gildið í þessum reit sýnir heildarmagn varanna í færslum á útleið sem eru með stöðuna _Frátekið fyrir pöntun_. Vörur sem eru fráteknar sem pantaðar eru ekki efnislega tiltækar í birgðum. Þess vegna er ekki hægt að tína þær beint og afhenda. |
| Tiltækt til frátekningar | Heildarmagn lagerbirgða sem hægt er að taka frá.<p>**Athugið:** Ef gátreiturinn **Taka frá pantaðar vörur** er valinn á síðunni **Færibreytur birgða- og vöruhúsakerfis**, inniheldur gildið í þessum reit væntanlegar innhreyfingar. Ef gátreiturinn er hreinsaður inniheldur gildið ekki væntanlegar innhreyfingar.</p> |
| Samtals magn til ráðstöfunar | Heildarmagn tiltækt.<p>**Samtals til ráðstöfunar** er reiknaður reitur. Gildið samsvarar gildinu **Efnislega tiltækt** að viðbættu gildinu **Samtals pantað** að frádregnu gildinu **Í pöntun**.</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>Nota síur til að finna færslur sem leitað er að

Notið svæðið **Síur** til að sía lista yfir lagerbirgðir þannig að hann innihaldi einungis færslur þar sem reitargildin samsvara síuskilyrðunum. Fylgið eftirfarandi skrefum til að skilgreina síu.

1. Á svæðinu **Síur** skal finna reitinn sem á að sía.
2. Í reitnum fyrir neðan heiti markreitsins skal velja rökvirkja (til dæmis, *hefst á*, *jafnt og*, eða *meira en*).
3. Sláið inn eða veljið gildið sem á að leita að.

> [!IMPORTANT]
> Síðan **Lagerlisti** er sett saman úr ítarlegri töflu yfir lagerbirgðir sem inniheldur allar tiltækar víddir. Listinn á þessari síðu er hins vegar samantekt. Hann gæti þar af leiðandi sameinað línur úr upprunatöflunni með því að leggja saman gildi samkvæmt víddunum sem eru sýndar.
>
> Síurnar sem eru skilgreindar á svæðinu **Síur** eiga við um upprunatöfluna, ekki samanlagða listann. Þessi hegðun getur stundum leitt til óvæntrar niðurstöðu. Upplýsingar um hvernig þessi hegðun getur haft áhrif á niðurstöðurnar er að finna í [dæmunum](#examples) seinna í þessu efnisatriði.
> 
> [Síurnar sem gefnar eru upp í hnitanetinu](#grid-filters) *eiga* hinsvegar við samanlagða listann. Þessar síur fela í sér bæði QuickFilter efst í hnitanetinu og síuna fyrir hvern dálkahaus.

Hægt er að breyta síusafninu sem er í boði á svæðinu **Síur** með því að fylgja eftirfarandi skrefum.

- Til að fjarlægja síu úr svæðinu skal tilheyrandi hnappinn **Loka** (**X**).
- Til að bæta við síu skal velja **Bæta við** efst á svæðinu **Síur**. Svarglugginn **Bæta við síureitum** sem birtist sýnir lista yfir tiltæka reiti. Hann sýnir einnig upplýsingar um gagnagerðina og töfluna fyrir hvern reit. Notið dálkahausana til að sía og raða listanum eftir þörfum og veljið síðan gátreitinn fyrir hvern reit sem á að bæta við svæðið **Sía**. Þegar þessu er lokið skal velja **Setja inn** til að gera breytingarnar.

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>Velja hvaða víddir á að sýna

Víddir segja meira til um hverja vöru í listanum yfir lagerbirgðir og bjóða upp á fleiri leiðir til að raða og sía listann. Víddirnar sem valið er að sýna hefur einnig áhrif á það hvernig línum er safnað saman á síðunni **Lagerlisti**. Þessi uppsöfnun getur í framhaldinu haft áhrif á það hvernig línur úr upprunatöflunum eru sameinaðar í niðurstöðunum sem birtast. Upplýsingar um hvernig þessi hegðun getur haft áhrif á niðurstöðurnar er að finna í [dæmunum](#examples) seinna í þessu efnisatriði.

Til að sérstilla val á birgðavíddum sem eru sýndar skal fylgja þessum skrefum.

1. Á aðgerðasvæðinu skal velja **Víddir**.

    Svarglugginn **Birting vídda** sem birtist sýnir allar víddir.

2. Veljið gátreitinn fyrir hverja vídd sem á að hafa með í hnitanetinu.
3. Ef ætlunin er að valið verði sjálfgefið notað næst þegar síðan **Lagerlisti** er opnuð, skal stilla valkostinn **Vista uppsetningu** á **Já**. Ef þessi valkostur er stilltur á **Nei** verður valið aðeins notað meðan á núgildandi lotu stendur. Þar af leiðandi verður núverandi sjálfgefið val notað næst þegar síðan verður opnuð.
4. Veljið **Í lagi** til að loka svarglugganum og gera breytingarnar.

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>Sía útkomu listans yfir lagerbirgðir

Hægt er að velja hvaða dálkahaus sem er í hnitanetinu **Á lager** til að raða eða sía eftir gildum í þeim dálki. QuickFilter efst í hnitanetinu býður upp á fleiri síuvalkosti. Þessar síur eiga við um niðurstöðurnar, ekki upprunatöfluna. Upplýsingar um hvernig þessi hegðun getur haft áhrif á niðurstöðurnar er að finna í [dæmunum](#examples) seinna í þessu efnisatriði.

> [!NOTE]
> Ekki er hægt að sía og raða eftir öllum dálkum. Flestir magndálkar innihalda ekki röðunar- og síunarstjórnun því að þeir eru reiknaðir reitir. Dálkurinn **Í pöntun** er undantekning.

## <a name="examples"></a><a name="examples"></a>Dæmi

Kerfið inniheldur nákvæma (ekki uppsafnaða) birgðatöflu sem sýnir eftirfarandi lagerbirgðir.

| Vörunúmer | Svæði | Vöruhús | Birgðir | Efnislegt magn til ráðstöfunar |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>Aðstæður 1

Síðan **Lagerlisti** er set upp til að sýna eftirfarandi lokavíddir:

- Vörunúmer
- Svæði
- Vöruhús

Á svæðinu **Síur** eru eftirfarandi síuskilyrði sett upp:

- **Vörunúmer** \| **er nákvæmlega** \| _IA0001_
- **Efnislega tiltækt** \| **minna en eða jafnt og** \| _1_

Hér er útkoman.

| Vörunúmer | Svæði | Vöruhús | Birgðir | Efnislegt magn til ráðstöfunar |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>Aðstæður 2

Síðan **Lagerlisti** er set upp til að sýna eftirfarandi lokavíddir:

- Vörunúmer
- Svæði

Á svæðinu **Síur** eru eftirfarandi síuskilyrði sett upp:

- **Vörunúmer** \| **er nákvæmlega** \| _IA0001_
- **Efnislega tiltækt** \| **minna en eða jafnt og** \| _1_

Hér er útkoman.

| Vörunúmer | Svæði | Birgðir | Efnislegt magn til ráðstöfunar |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

Athugið að stillingarnar á svæðinu **Síur** eiga við um ítarlegu (ekki uppsafnaða) birgðatöfluna sem er sýnd í upphafi þessa hluta. Þar af leiðandi finnur skilyrðið **Efnislega tiltækt** \| **minna en eða jafnt og** \| _1_ tvær línur úr þeirri töflu (fyrstu og þriðju línu, sem hvor um sig sýnir gildi fyrir **Efnislega tiltækt** upp á _1_). Hins vegar, í þessu dæmi, er síðan **Lagerlisti** ekki sett upp til að sýna víddina **Vöruhús**. Þar af leiðandi leggur það upprunalegu línurnar tvær saman í eina línu því að báðar línurnar eru með sama gildið í öllum víddunum sem sýndar eru. Þessi lína virðist ekki fara eftir síuskilyrðinu vegna þess að gildið **Efnislega tiltækt** er sýnt sem _2_. Niðurstaðan er hinsvegar rétt vegna þess að stillingarnar á svæðinu **Síur** eiga við um upprunatöfluna, ekki samanlögðu töfluna sem er sýnd á síðunni **Lagerlisti**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]