---
title: Undirbúningur fyrir keyrslu á Human Resources
description: Á þessari síðu er að finna leiðbeiningar um hvernig á að undirbúa sig fyrir keyrslu á Dynamics 365 Human Resources.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59d7274c3b40e78209d90960c4514321b736876a
ms.sourcegitcommit: b40d6ce45aeb07724fc41d1a41923970b007fbcf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2020
ms.locfileid: "4419099"
---
# <a name="prepare-for-human-resources-go-live"></a>Undirbúningur fyrir keyrslu á Human Resources

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er því lýst hvernig á að undirbúa keyrslu á Dynamics 365 Human Resources-verki með því að nota Microsoft Dynamics Lifecycle Services. 

Þessi mynd sýnir þrepin í keyrsluferlinu. 

![Ferli keyrslu](./media/hr-admin-go-live-prepare-process.png)

Í eftirfarandi töflu er listi yfir öll skrefin í ferlinu, væntanleg tímalengd og hver ber ábyrgð á aðgerðinni.

| Áfangi | Aðgerð | Tímalengd/hvenær | Hver | Athugasemdir |
| --- | --- | --- | --- |--- |
| 1 | Uppfæra keyrsludagsetningu í LCS | Í síðasta lagi með 2-3 mánaða fyrirvara | Samstarfsaðili/viðskiptavinur | Áfangadagsetningum skal haldið uppfærðum með reglulegu millibili. |
| 2 | Ljúka við og senda gátlista | Eftir að samþykkisprófun notanda er lokið | Samstarfsaðili/viðskiptavinur | Fylgja skal leiðbeiningunum í [Keyrslumat FastTrack](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Verkmat (FastTrack) | Hönnuður FastTrack* | Hönnuður kemur með mat þegar gátlisti er móttekin og heldur áfram yfirferð þar til spurningum hefur verið svarað og flutningar eru tilbúnir ef það á við. |
| 4 | Vinnustofa verks (FastTrack) | Hönnuður FastTrack* | |
| 5 | Innflutningur gagnapakka | Fer eftir verkinu | Samstarfsaðili/viðskiptavinur | Fylgja skal leiðbeiningunum í [Yfirliti gagnastjórnunar](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).|
| 6 | Vinnsla tilbúin | Þegar öllum fyrri skrefum er lokið | Samstarfsaðili/viðskiptavinur | Samstarfsaðili/viðskiptavinur getur tekið við stjórn vinnsluumhverfisins.|
| 7 | Flutningsaðgerðir | Fer eftir verkinu | Samstarfsaðili/viðskiptavinur | |
| 8 | Ljúka | Fer eftir verkinu | Viðskiptavinur | |

> [!IMPORTANT]
> *Skrefum 3 og 4 er aðeins lokið fyrir viðskiptavini sem uppfylla skilyrði FastTrack.

## <a name="completing-the-lcs-methodology"></a>Lokið við LCS-aðferðina

Stór áfangi í hverju innleiðingarverki fyrir sig er flutningur yfir í vinnsluumhverfið. 

Til að tryggja að vinnsluumhverfið sé notað fyrir virkar aðgerðir, úthlutar Microsoft aðeins vinnsluumhverfinu þegar innleiðingin nálgast áfangann **Stjórna** þegar áskildum aðgerðum í LCS-aðferðinni er lokið. Frekari upplýsingar um umhverfin í áskriftinni þinni er að finna í  [Leyfishandbók Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544). 

Viðskiptavinir verða að ljúka við áfangana **Greining**, **Hanna og þróa** og **Prófa** í LCS-aðferðinni áður en  **Skilgreina** hnappurinn til að biðja um vinnsluumhverfið verður aðgengilegur. Til að ljúka áfanga í LCS verður fyrst að ljúka öllum nauðsynlegum skrefum í þeim áfanga. Þegar öllum skrefum í áfanga er lokið er hægt að ljúka öllum áfanganum. Alltaf er hægt að opna áfanga aftur síðar ef gera þarf breytingar. Frekari upplýsingar er að finna í  [Viðskiptavinir Lifecycle Services (LCS) fyrir Finance and Operations forrit](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs). 

Ferlið við að ljúka við skref er með tvo hluta: 

- Gerið raunverulega vinnu, svo sem greining á samsvörun og gloppum eða samþykkisprófun notanda. 
- Merktu samsvarandi skref í LCS-aðferðinni sem lokið. 

Gott er að ljúka við skrefin í aðferðinni eftir því sem innleiðingunni vindur fram. Ekki bíða þar til á síðustu stundu. Ekki bara smella í gegnum öll skrefin til að fá vinnsluumhverfi. Það er í hag viðskiptavinarins að fá áreiðanlega innleiðingu. 

## <a name="uat-for-your-solution"></a>Samþykkisprófun notanda (UAT) fyrir lausnina þína

Í UAT-áfanganum þarf að prófa alla viðskiptaferla sem hafa verið innleiddir og allar sérstillingar sem gerðar hafa verið í sandkassaumhverfi í innleiðingarverkinu. Til að tryggja vel heppnaða keyrslu ætti að íhuga eftirfarandi þegar lögð er lokahönd á UAT-áfangann: 

- Prófunartilvik ná yfir allar kröfurnar. 
- Prófaðu með því að nota flutt gögn. Þessi gögn ættu að innihalda aðalgögn, svo sem starfsmenn, störf og stöður. Taktu einnig með opnunarstöður eins og uppsöfnuð leyfi og fjarvistir. Að lokum skal taka með opnar færslur eins og gildandi fríðindaskráningar. Ljúkið prófun á öllum gagnagerðum, jafnvel þótt gagnasafninu sé ekki lokið. 
- Prófið með því að nota rétt öryggishlutverk (sjálfgefin hlutverk og sérstillt hlutverk) sem er úthlutað á notendur. 
- Gakktu úr skugga um að lausnin samræmist öllum kröfum sem tengjast fyrirtæki og atvinnugrein. 
- Skjalfestu alla eiginleika og fáðu samþykki frá viðskiptavininum. 

## <a name="fasttrack-go-live-assessment"></a>Keyrslumat FastTrack

Viðskiptavinir sem uppfylla skilyrði FastTrack og eru í samvinnu við úrlausnarhönnuð FastTrack munu ljúka yfirferð á keyrslu með Microsoft FastTrack. Frekari upplýsingar er að finna í  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). 

Um átta vikum fyrir keyrslu mun FastTrack-teymið biðja þig um að fylla út [Gátlisti fyrir keyrslu](https://go.microsoft.com/fwlink/?linkid=2146013).

Verkefnisstjórinn eða helsti aðilinn að verkinu verður að ljúka við gátlisti fyrir keyrslu í áfanga forkeyrslu fyrir verkið. Yfirleitt er gátlistanum lokið fjórum til sex vikum á undan uppgefinni keyrsludagsetningu, þegar samþykkisprófun notanda er lokið eða næstum lokið. 

Þegar þú hefur lokið við gátlista fyrir keyrslu skaltu senda hann til úrlausnarhönnuðar FastTrack í tölvupósti. Láttu alltaf helsta hagsmunaaðila viðskiptavinarins og samstarfsaðila innleiðingarinnar fylgja með í tölvupóstinum. 

Þegar búið er að senda inn gátlistann mun úrslausnarhönnuður FastTrack fara yfir verkið og leggja fram mat sem útlistar mögulegar áhættur, bestu starfsvenjur og ráðleggingar fyrir vel heppnaða keyrslu verksins. Í sumum tilvikum gæti úrlausnarhönnuðurinn lagt áherslu á áhættuþætti og beðið um flutningsáætlun. 

## <a name="see-also"></a>Sjá einnig

[Algengar spurningar um keyrslu](hr-admin-go-live-faq.md)