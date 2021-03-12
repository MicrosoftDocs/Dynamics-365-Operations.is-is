---
title: Vinna með sniðmát
description: Þetta efni lýsir því hvernig á að vinna með sniðmát í Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f4ed3b6797127113450949aa957437125f37394f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995717"
---
# <a name="work-with-templates"></a>Vinna með sniðmát


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að vinna með sniðmát í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Eins og fjallað var um í [Yfirlit yfir sniðmát og skipulag](templates-layouts-overview.md) skilgreina sniðmát hópinn af valkostum sem eru tiltækir höfundum. Sniðmát eru gagnleg fyrir vefhöfundateymi fyrirtækisins af ýmsum ástæðum og vel skipulögð sniðmát geta hjálpað við öll eftirfarandi markmið:

- Einfalda höfundarupplifunina fyrir daglega hlutverk ritstjóra.

    - Sía valkosti fyrir einingar þannig að aðeins viðeigandi einingar séu sýndar fyrir ákveðinn hluta blaðsíðu. (Til dæmis er hægt að stilla markaðshluta sniðmáts til að sía út óviðkomandi einingar sem aldrei ætti að nota í því samhengi og sem munu bara flækja höfundaverk efnis ef þau eru sýnd.)
    - Stilla sjálfgefna einingarstillingu til að bæta skilvirkni höfunda.
    - Skilgreindu sjálfgefin síðubrot til að bæta skilvirkni höfunda. (Til dæmis birtast fyrirsagnar- og síðufótabrot í sniðmáti sjálfkrafa á hverri hlið síðunnar.)

- Haltu fyrirtækjasíðum á vörumerkinu með því að skilgreina samþykkt sett af fyrirkomulagi eininga og stillingar.

    > [!TIP] 
    > Árangursrík netverslunarsvæði veita viðskiptavinum kunnugleg, endurtekin og vörumerkjanotendamynstur notendaupplifunar (UX). Með því að nota sniðmát hjálpar þú til við að stjórna samræmi á vefsvæðinu þínu.

- Bætið stig leitarvélabestun (SEO) með því að tryggja endurteknar og forritaðar skilgreiningar á síðu og lýsigögnum.

> [!NOTE]
> Þrátt fyrir að sniðmát séu hönnuð til að stjórna samræmi á vefsvæði, þá er fræðilega hægt að stilla þau þannig að þau fylgi engu samræmi. Stjórnendur vörumerkis og vefsvæða geta skilgreint hvaða stig sem er á breytileika fyrir síðurnar á vefsvæðinu. Til dæmis er hægt að láta sniðmát vera alveg opið þannig að höfundar efnis geta búið til hvaða síðuhönnun sem þeir velja. Í þessu tilfelli eiga engir af kostunum á listanum hér á undan við.

## <a name="modify-a-template"></a>Breyta sniðmáti

Sniðmátum er breytt með því að nota sniðmátsritil.

Fylgdu einu af þessum skrefum til að opna sniðmátstitilinn:

- Í yfirlitssvæðinu á svæðinu velurðu **Sniðmát** og síðan velurðu sniðmátið sem á að breyta.
- Í síðuritlinum fyrir fyrirliggjandi síðu velurðu efsta hnútinn í útlínutré til vinstri. Síðan, í eiginleikaglugganum til hægri, velurðu eiginleikann **Breyta sniðmáti**.

Útlínutréð til vinstri sýnir valkosti og uppbyggingu einingar sem eru í boði fyrir undirskipulag og síður. Þegar þú velur einingu í útlínutréð geturðu skoðað sniðmátseiginleika valinnar einingar í eiginleikaglugganum til hægri. Sumir af þessum eiginleikum eru einkvæmir fyrir sniðmátsbreytingu. Eftirfarandi tafla lýsir þessum eiginleikum.

| Nafn eiginleika | Lýsing |
|---|---|
| Lágmark atvika | Þessi eiginleiki skilgreinir lágmarksfjölda viðburða fyrir valda einingu. Til dæmis ef gildi er stillt á **1** er einingarinnar krafist fyrir höfunda í forstreymi, en ef gildið er stillt á **0** (núll) er einingin valkvæð. |
| Hámark atvika | Þessi eiginleiki skilgreinir hámarksfjölda viðburða fyrir valda einingu. Til dæmis ef gildi er stillt á **1** er aðeins hægt að bæta einingunni einu sinni við. |
| Lágm.einingar (gámar) | Fyrir einingar sem innihalda aðrar einingar (það er fyrir *gámaeiningar*) skilgreinir þessi eiginleiki lágmarksfjölda heildareininga sem ætti að bæta við sem undireiningum. Til dæmis, fyrir hringekjueiningu gæti gildið verið stillt á tölu sem er hærri en 1. |
| Hám.einingar (gámar) | Fyrir gámaeiningar skilgreinir þessi eiginleiki hámarksfjölda heildareininga sem ætti að bæta við sem undireiningum. Til dæmis, fyrir hringekjueiningu gæti gildið verið stillt á tölu sem er lægri en 10. |
| Læst | Boolean-stýringin **Læst** birtist við hliðina á öllum eiginleikum kjarnaeininga. Hún gerir sniðmátshöfundi kleift að læsa einingastillingu í sniðmátinu. Einingastillingu sem er læst er ekki hægt að hnekkja af neinum undirskipulagi eða síðum. Hún verður miðlægt breytanlegt eiginleikagildi fyrir allt skipulag og síður sem nota sniðmátið. |

## <a name="create-a-new-template"></a>Búa til nýtt sniðmát

Fylgið eftirfarandi skrefum til að stofna nýtt sniðmát.

1. Í yfirlitssvæðinu á svæðinu velurðu **Sniðmát** til að opna skjá sniðmátseftirlitsaðila.
1. Velja **Nýtt sniðmát**.
1. í valmynd fyrir stofnun sniðmáts er fært inn nafn og lýsing fyrir sniðmátið. Gildin sem þú slærð inn verða sýnd höfundum þegar þeir búa til nýjar síður. Sláðu því inn lýsigögn sem munu nýtast síðuhöfundum. Til dæmis, sláðu inn **Notaðu þetta sniðmát til að búa til almennar markaðssíður** sem lýsinguna. Þessum lýsigögnum er hægt að breyta síðar.
1. Veldu **Í lagi** til að búa til nýja sniðmátið og opna sniðmátsritil. Sniðmátsritill sýnir útlínutré til vinstri og eiginleikaglugga til hægri.
1. Stækkaðu hnútana í útlínutrénu og veldu hólfið **HTML-haus**.
1. Ef engar einingar eru enn komnar í þetta hólf skaltu velja úrfellingarhnappinn (**...**) og veldu síðan **Bæta við einingu**.
1. Í svarglugganum **Bæta við einingu** skal velja **Sjálfgefið síðuyfirlit** og síðan smella á **Í lagi**.
1. Veldu útlitseðilinn í útlínutrénu og sláðu síðan inn í eiginleikaglugganum allar sjálfgefnar stillingar sem sjálfkrafa ætti að stilla fyrir allar undirsíður sniðmátsins. Ef þú vilt ekki neinar sjálfgefnar stillingar skaltu láta gildin vera auð.
1. Í síðuútlínunum velurðu hólfið **Meginmál**, velur úrfellingarhnappinn og velur síðan **Bæta við einingu**.
1. Veldu einingu síðugáms (það gæti verið aðeins einn valkostur) og veldu síðan **Í lagi**.

Undir nýju gámaeiningunni muntu sjá nýtt sett af hólfum (**Fyrirsögn**, **Aðal**, og svo framvegis). Hér getur þú bætt við og stillt einingavalkostina sem verða tiltækir höfundum þegar þeir búa til síður úr þessu sniðmáti. Sjálfgefið er að ef þú bætir engum einingum við hólf eru allar tiltækar gerðir eininga studdar fyrir það hólf.

Sniðmátið er nú tæknilega gilt og það er hægt að vista, haka við og nota til að búa til nýjar síður. Næstu þrír hlutar lýsa þó nokkrum öðrum sjálfgefnum stillingum sem þú vilt kannski stilla fyrst.

## <a name="add-a-header-and-a-footer"></a>Bæta við fyrirsögn og síðufæti

Ef síða þín er þegar með fyrirsagnarbrot skaltu fylgja þessum skrefum til að bæta fyrirsögn og síðufæti við sniðmát.

1. Í útlínutrénu stækkarðu hólfið **Meginmál** og undirsíðueiningu þess.
1. Veldu hólfið **Fyrirsögn**.
1. Veldu úrfellingarhnappinn fyrir hólfið **Fyrirsögn** og veldu síðan **Bæta við broti**.
1. Leitaðu að og veldu fyrirsagnarbrot svæðisins og veldu síðan **Í lagi**.

Allar síður sem nota sniðmátið erfa nú sjálfkrafa þetta fyrirsagnarbrot.

Ef vefsvæðið þitt er ekki enn með fyrirsagnarbrot skaltu sjá [Stofna brot](work-with-fragments.md#create-a-fragment) til að fá upplýsingar um hvernig á að búa til það og ljúka síðan fyrra ferli.

## <a name="change-the-template-theme"></a>Breyta sniðmátsþemanu

Fylgdu þessum skrefum til að stilla sjálfgefið þema fyrir allar síður sem nota sniðmát.

1. Í útlínutré síðunnar til hægri stækkarðu hólfið **Meginmál**.
1. Í hólfinu **Meginmál** velurðu síðugámaeininguna (til dæmis, **Sjálfgefin síða**).
1. Í eiginleikaglugganum hægra megin, í reitnum **Þema**, velurðu þema.

Sjálfgefið er að allar nýjar síður munu nú nota valið þema. Til að koma í veg fyrir að síður hnekki þessari stillingu á skipulagi eða á síðustigi stillirðu Boleean-stýringuna **Læst** á **Satt**.

## <a name="add-a-script-to-a-template"></a>Bæta handriti við sniðmát

Þú getur bætt við HTML **&lt;forskrift&gt;** þætti sem inniheldur JavaScript í sniðmátinu þínu. Á þennan hátt geturðu framkvæmt sjálfgefna forskriftarhegðun á HTML haus, upphaf meginmáls og meginmálslokahluta síðanna.

Fylgið eftirfarandi skrefum til að bæta forskrift við sniðmát.

1. Í útlínutrénu til vinstri velurðu hólfið þar sem þú vilt bæta við þættinum **&lt;forskrift&gt;** (til dæmis, HTML haus, upphafi meginmáls eða lokum meginmáls).
1. Veldu úrfellingarhnappinn fyrir hólfið og veldu síðan **Bæta við einingu**.
1. Í valmyndinni **Bæta við einingu** velurðu forskriftareiningu (t.d. **Ytri forskrift** eða **Innbyggð forskrift**).
1. Í eiginleikaglugganum til hægri, í viðkomandi eiginleikastýringu forskriftar (til dæmis, **Innbyggð forskrift** eða **Forskriftarmerki**), slærðu inn forskriftina.
1. Sláðu inn allar aðrar valfrjálsar stillingar sem þú vilt stilla á eiginleikaglugganum.

> [!TIP]
> Ef þú vilt endurnýta einhverja af forskriftareiningunum þínum fyrir önnur sniðmát, geturðu breytt þeim í brot. Á þennan hátt hjálpar þú til við að gera höfundarferlið skilvirkara og þú gerir uppfærsluferlið miðlægt. Fyrir upplýsingar um hvernig á að umbreyta handritseiningu í brot skal sjá [Vista fyrirliggjandi einingastillingu sem brot](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).

## <a name="save-check-in-preview-and-publish-a-template"></a>Vistaðu, skráðu inn, forskoðaðu og birtu sniðmát.

Til að vista sniðmát og skrá það inn skal fylgja þessum skrefum.

1. Veldu **Vista** efst í sniðmátsritli. Vistaðar breytingar hafa ekki áhrif á forstreymissíðum fyrr en þær eru skráðar inn.
1. Veldu **Ljúka við breytingar**. Nú er hægt að uppgötva breytingarnar fyrir forstreymisflæði.

Til að forskoða breytingarnar skaltu annaðhvort opna fyrirliggjandi síðu sem notar sniðmátið eða búa til nýja síðu úr sniðmátinu.

Eftir að þú hefur forskoðað breytingarnar á sniðmátinu skaltu fylgja einu af þessum skrefum til að birta sniðmátið á lifandi vefsvæði:

* Farðu í **Sniðmát**, veldu sniðmátið og veldu síðan **Birta**.
* Veldu útlitsheiti til að opna útlitsritil og veldu svo **Birta**.
* Birta síðu sem vísar til óbirta sniðmátsins. Sniðmátið er sjálfkrafa birt.

> [!WARNING]
> Þegar sniðmát, eða eitthvað annað atriði efnisstjórnunarkerfis (CMS), er birt er það hægt að uppgötva á internetinu. Ekki birta skjöl eða eignir fyrr en þú ert tilbúin/n til að gera þau opinber. Skjalaútgáfur sem hafa verið vistaðar og skráðar inn, en sem ekki hafa verið birtar, er aðeins hægt að sjá fyrir staðfesta kerfisnotendur.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md)

[Vinna með forstillt útlit](work-with-layouts.md)
