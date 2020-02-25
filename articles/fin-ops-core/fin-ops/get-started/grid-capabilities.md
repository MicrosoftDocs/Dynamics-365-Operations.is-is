---
title: Hnitanetsgeta
description: Þetta efni lýsir nokkrum kröftugum eiginleikum netstýringar. Það verður að gera nýja hnitanetsaðgerðina kleift að hafa aðgang að þessum möguleikum.
author: jasongre
manager: AnnBe
ms.date: 01/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b49d7823f48bcc9cdbb56b87d5fa72d46ddfa15c
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019831"
---
# <a name="grid-capabilites"></a>Hnitanetsgeta

[!include [banner](../includes/banner.md)]

Nýja netstýringin veitir fjölda gagnlegra og öflugra getu sem hægt er að nota til að auka framleiðni notenda, smíða áhugaverðari sýn á gögnin þín og fá þroskandi innsýn í gögnin þín. Þessi grein mun fjalla um eftirfarandi getu: 

-  Reiknar samtölur
-  Flokkun gagna
-  Vélritun á undan kerfinu
-  Mat á stærðfræðisegðum 

## <a name="calculating-totals"></a>Reiknar samtölur
Í forritum Finance and Operations geta notendur séð heildartölur neðst í töludálkum í hnitanetum. Þessar samtölur eru sýndar í síðufótarhluta neðst á töflunni. 

### <a name="showing-the-grid-footer"></a>Sýni síðufót hnitanetsins
Sérhver töflunet í forritum Finance and Operations er með fótarsvæði neðst á töflunni sem getur sýnt mikilvægar upplýsingar sem tengjast gögnum sem birt eru. Þessar upplýsingar fela í sér: 
-  Fjöldi valda lína í töflunni (þegar fleiri en ein skrá er valin)
-  Stórt heildartölur neðst í samstilltu tölugildum
-  Fjöldi raða í gagnasafninu 

Þessi fótur er sjálfgefið falinn en auðvelt er að kveikja á honum. Til að sýna fót fyrir rist, hægrismellt er á dálkhaus í töflunni og valið valkosturinn **Sýna fót**. Þegar búið er að kveikja á fótfótum fyrir tiltekið rist mun sú stilling muna þar til notandinn kýs að fela fótfótinn, það er hægt að gera með því að hægrismella á dálkhaus og velja **Fela fót**.  Athugið staðsetningu staðsetningu **Sýna fót / Fela fót** Búist er við að aðgerð verði staðsett aftur í framtíðaruppfærslu. 

### <a name="specifying-columns-with-totals"></a>Tilgreina dálka með samtölum
Sem stendur er enginn dálkur stilltur til að sýna samtöl sem sjálfgefið. Þess í stað er þetta talið einskiptisvirkni, svipað og að laga breidd dálka í ristum. Þegar þú hefur tilgreint að þú viljir sjá samtölur fyrir dálk, þá munst þessi stilling næst þegar þú heimsækir síðuna.  

Það eru tvær leiðir til að stilla dálk til að sýna samtals: 
1.  Hægrismelltu á dálkinn sem þú hefur áhuga á að sjá samtals fyrir og veldu **Samtals þennan dálk**. Þessi aðgerð mun gera þrennt. Í fyrsta lagi mun það gera fótinn sýnilegan. Í öðru lagi mun það spara ósk þína um að sjá samtals í þessum dálki. Í þriðja lagi mun þessi aðgerð hefja heildarútreikning fyrir þennan dálk og þá aðra sem þú hefur áður stillt til að sjá heildartölur. Tíminn sem það tekur að samtals sé sýndur er beintengdur stærð gagnapakkans sem þú ert að samtals.  

2.  Þegar fótur hefur verið sýndur geturðu valið að smella á **Sýna samtals** hnappinn í fótfótasvæðinu neðst í dálkinum sem þú hefur áhuga á að sjá samtals fyrir. Ef það eru engar stilla dálka, þá **Sýna samtals** hnappur verður sýnilegur fyrir alla talnardálka. Þegar að minnsta kosti einn dálkur er stilltur fyrir samtöl, **Sýna samtals** hnappar verða aðeins fáanlegir á sveimi eða fókus. Þessi aðgerð vistar einfaldlega ósk þína um að sjá samtals í þessum dálki fyrir komandi heimsóknir á þessa síðu, og þetta ástand er gefið til kynna með bandstrikinu sem birtist í þessum dálki í fótfótum (eða samtals birtist strax ef gagnapakkinn er nægilega lítill) .

Ef þú gerir mistök og vilt ekki lengur sjá samtals í tilteknum dálki, hægrismellt á dálkinn og veldu **Fela samtals** eða veldu **Fela samtals** hnappinn í síðufætinum í þeim dálki. Þessi valkostur verður einnig vistaður fyrir framtíðarheimsóknir á síðunni. 

### <a name="calculating-totals"></a>Reiknar samtölur
Þegar þú kemur á síðu þar sem fótstigið er sýnilegt og dálkar nú þegar stilltir fyrir heildartölur, eru heildartölur mögulega eða ekki sýndar í fótfætinum. Hegðunin er háð stærð gagnapakkans á síðunni. Ef gagnapakkinn er nægjanlega lítill, birtast samtöl sjálfkrafa ásamt fjölda lína í gagnapakkanum. Ef það eru bandstrik í fótfótum undir dálkunum sem þú stilltir fyrir heildartölur, þá er gagnapakkinn of stór til að kerfið geti sýnt heildartölur strax og þörf er á skýrum aðgerðum til að reikna heildartölurnar. Til að gera þetta, smelltu á **Reikna** hnappinn í fótfótinum, eða hægrismelltu á dálkinn sem þú vilt hafa samtals fyrir og veldu **Samtals þennan dálk**.  

Ef útreikningurinn tekur of langan tíma geturðu hætt við aðgerðina með því að velja **Hætta við** takki. Stundum verður gagnapakkinn þó of stór til að reikna út heildartölur (takmörk sett af fyrirtækinu) og þér verður tilkynnt að sía gögnin þín meira.

Heildartölur munu uppfærast sjálfkrafa þegar þú uppfærir, eyðir eða býrð til línur í gagnapakkanum.  

## <a name="grouping-data"></a>Flokkun gagna
Notendur fyrirtækja þurfa oft að framkvæma sértækar greiningar á gögnum. Þó að þetta sé hægt að gera með því að flytja gögn út til Microsoft Excel og nota pivot töflur, the **Flokkun** getu í töflum ristum gerir notendum kleift að skipuleggja gögn sín á áhugaverðan hátt innan Finance and Operations smáforrit. Eins og þessi aðgerð nær til **Heildartölur** lögun, **Flokkun** gerir þér einnig kleift að fá þroskandi innsýn í gögnin með því að gefa undirstig á hópsstigi.

Til að nota þennan eiginleika skaltu hægrismella á dálkinn sem þú vilt flokka eftir og velja **Flokkaðu eftir þessum dálki**. Þessi aðgerð mun raða gögnum eftir völdum dálki, bæta við nýjum hóp eftir dálki í byrjun í ristina og setja „hausraðir“ í byrjun hvers hóps. Þessar hausraðir veita eftirfarandi upplýsingar um hvern hóp: 
-  Gagnagildi fyrir hópinn 
-  Dálkamerki. Þetta mun vera sérstaklega gagnlegt þegar mörg stig hóps eru studd.  
-  Fjöldi gagnalína í þessum hópi
-  Undirmál fyrir hvaða dálk sem er stilltur til að sýna samtölur

Með [Vistaðar skoðanir](saved-views.md) virkt, þá er hægt að vista þennan flokkun með sérstillingu sem hluta af útsýni til að fá skjótan aðgang næst þegar þú heimsækir síðuna.  

Ef þú velur **Flokkaðu eftir þessum dálki** í öðrum dálki verður upprunalegum hópum skipt út, þar sem aðeins stig hóps er stutt í 10.0.9 / uppfærslu pallsins 33.

Til að afturkalla flokkun í rist skaltu hægrismella á flokkunarsúluna og velja **Taka saman hóp**.  


## <a name="evaluating-math-expressions"></a>Mat á stærðfræðisegðum
Sem framleiðniörvun getur notandi slegið stærðfræðiformúlur inn í tölulegar frumur í rist í stað þess að þurfa að gera útreikninginn í forriti utan kerfisins. Til dæmis geturðu slegið inn **=15\*4** og flipaðu út af sviði. Kerfið mun meta tjáninguna og vista gildi „60“ fyrir reitinn.

Til að gera kerfið að viðurkenna gildi sem tjáningu, byrjaðu gildið með jöfnu merki (**=**). Nánari upplýsingar um rekstraraðila sem studd er og setningafræði, sjá [Studd stærðfræðitákn](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols).  
