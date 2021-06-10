---
title: Undirbúningur fyrir keyrslu á Human Resources
description: Á þessari síðu er að finna leiðbeiningar um hvernig á að undirbúa sig fyrir keyrslu á Dynamics 365 Human Resources.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dcec7963bdf70f848249bb2ca5e2208e09f49548
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054789"
---
# <a name="prepare-for-human-resources-go-live"></a>Undirbúningur fyrir keyrslu á Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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
| 5 | Innflutningur gagnapakka | Fer eftir verkinu | Samstarfsaðili/viðskiptavinur | Fylgja skal leiðbeiningunum í [Yfirliti gagnastjórnunar](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).|
| 6 | Vinnsla tilbúin | Þegar öllum fyrri skrefum er lokið | Samstarfsaðili/viðskiptavinur | Samstarfsaðili/viðskiptavinur getur tekið við stjórn vinnsluumhverfisins.|
| 7 | Flutningsaðgerðir | Fer eftir verkinu | Samstarfsaðili/viðskiptavinur | |
| 8 | Ljúka | Fer eftir verkinu | Viðskiptavinur | |

> [!IMPORTANT]
> *Skrefum 3 og 4 er aðeins lokið fyrir viðskiptavini sem uppfylla skilyrði FastTrack.

## <a name="completing-the-lcs-methodology"></a>Lokið við LCS-aðferðina

Stór áfangi í hverju innleiðingarverki fyrir sig er flutningur yfir í vinnsluumhverfið. Ferlið við að ljúka við skref er með tvo hluta: 

- Gerið raunverulega vinnu, svo sem greining á samsvörun og gloppum eða samþykkisprófun notanda. 
- Merktu samsvarandi skref í LCS-aðferðinni sem lokið. 

Gott er að ljúka við skrefin í aðferðinni eftir því sem innleiðingunni vindur fram. Ekki bíða þar til á síðustu stundu. Það er í hag viðskiptavinarins að fá áreiðanlega innleiðingu. 

## <a name="uat-for-your-solution"></a>Samþykkisprófun notanda (UAT) fyrir lausnina þína

Í UAT-áfanganum þarf að prófa alla viðskiptaferla sem hafa verið innleiddir og allar sérstillingar sem gerðar hafa verið í sandkassaumhverfi í innleiðingarverkinu. Til að tryggja vel heppnaða keyrslu ætti að íhuga eftirfarandi þegar lögð er lokahönd á UAT-áfangann: 

- Mælt er með því að UAT-ferlið byrji á hreinu og fersku umhverfi þar sem gögnin úr GOLD-grunnstillingunni eru afrituð í umhverfið áður en UAT-ferlið er hafið. Mælt er með því að nota framleiðsluumhverfið sem GOLD-umhverfið fram að keyrslu, en á þeim tímapunkti verður umhverfið að framleiðsluumhverfi.
- Prófunartilvik ná yfir allar kröfurnar. 
- Prófaðu með því að nota flutt gögn. Þetta ætti að innihalda gögn á borð við starfskrafta, störf og stöður. Taktu einnig með opnunarstöður eins og uppsöfnuð leyfi og fjarvistir. Að lokum skal taka með opnar færslur eins og gildandi fríðindaskráningar. Ljúkið prófun á öllum gagnagerðum, jafnvel þótt gagnasafninu sé ekki lokið. 
- Prófið með því að nota rétt öryggishlutverk (sjálfgefin hlutverk og sérstillt hlutverk) sem er úthlutað á notendur. 
- Gakktu úr skugga um að lausnin samræmist öllum kröfum sem tengjast fyrirtæki og atvinnugrein. 
- Skjalfestu alla eiginleika og fáðu samþykki frá viðskiptavininum. 

## <a name="mock-go-live"></a>Herma eftir keyrslu

Á undan keyrslu þarf að framkvæma hermikeyrslu til að prófa skrefin sem þarf að taka til að fara úr gamla kerfinu og yfir í það nýja. Framkvæma ætti hermikeyrsluna í sandkassaumhverfi og hafa með öll skrefin í flutningsáætluninni.

- Við mælum með því að nota vinnsluumhverfið sem umhverfi GOLD-grunnstillingar fram að keyrslu.
- Ganga þarf úr skugga um að öflugt stjórnunarferli sé til staðar til að vernda vinnsluumhverfið fyrir óvæntum færslum eða uppfærslum áður en keyrsla er gerð.
- Þegar UAT eða hermikeyrsla er tilbúin skal uppfæra sandkassaumhverfið í vinnsluumhverfinu. Frekari upplýsingar má finna í [Afrita tilvik](hr-admin-setup-copy-instance.md).
- Prófa skal hvert skref í flutningsáætluninni í sandkassaumhverfinu og síðan villuleita sandkassaumhverfið með því að framkvæma stikkprufur eða prófanir úr UAT-forskriftum í umhverfinu.
  - Prófanir eiga að fela í sér gagnaflutninga, þ.m.t. nauðsynlegar umbreytingar fyrir keyrsluna.
  - Ferlið á að fela í sér prufuflutning á einhverju gömlu kerfi.
  - Gætið þess að hafa með skref samþættingarflutnings eða ytri skref kerfis í hermiflutningnum.
- Ef upp koma einhver vandamál í hermiflutningnum þarf að gera annan hermiflutning. Af þeim sökum er mælt með að áforma tvo hermiflutninga í verkáætluninni.

## <a name="fasttrack-go-live-assessment"></a>Keyrslumat FastTrack

Viðskiptavinir sem uppfylla skilyrði FastTrack og eru í samvinnu við úrlausnarhönnuð FastTrack munu ljúka yfirferð á keyrslu með Microsoft FastTrack. Frekari upplýsingar er að finna í  [Microsoft FastTrack](/dynamics365/fasttrack/). 

Um átta vikum fyrir keyrslu mun FastTrack-teymið biðja þig um að fylla út [Gátlisti fyrir keyrslu](https://go.microsoft.com/fwlink/?linkid=2146013).

Verkefnisstjórinn eða helsti aðilinn að verkinu verður að ljúka við gátlisti fyrir keyrslu í áfanga forkeyrslu fyrir verkið. Yfirleitt er gátlistanum lokið fjórum til sex vikum á undan uppgefinni keyrsludagsetningu, þegar samþykkisprófun notanda er lokið eða næstum lokið. 

Þegar þú hefur lokið við gátlista fyrir keyrslu skaltu senda hann til úrlausnarhönnuðar FastTrack í tölvupósti. Láttu alltaf helsta hagsmunaaðila viðskiptavinarins og samstarfsaðila innleiðingarinnar fylgja með í tölvupóstinum. 

Þegar búið er að senda inn gátlistann mun úrslausnarhönnuður FastTrack fara yfir verkið og leggja fram mat sem útlistar mögulegar áhættur, bestu starfsvenjur og ráðleggingar fyrir vel heppnaða keyrslu verksins. Í sumum tilvikum gæti úrlausnarhönnuðurinn lagt áherslu á áhættuþætti og beðið um flutningsáætlun. 

## <a name="see-also"></a>Sjá einnig

[Algengar spurningar um keyrslu](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
