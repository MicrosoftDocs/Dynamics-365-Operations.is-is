---
title: Staðgreiðsluskattsskýrsla fyrir Egyptaland
description: Þetta efnisatriði útskýrir hvernig á að skilgreina og mynda staðgreiðsluskattsskýrslu fyrir Egyptaland.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8c9aaa3868167806ce3189d724621991ec7e53eb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022812"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>Staðgreiðsluskattsskýrsla fyrir Egyptaland (EG-00005)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Yfirlit
Þetta efnisatriði útskýrir hvernig á að setja upp og mynda staðgreiðsluskattskýrslu og eyðublöð staðgreiðsluskattskýrslu 41 og 11 fyrir lögaðila í Egyptalandi 

Allar egypskar einingar verða að undirbúa eyðublað 41, sem tekur saman alla skatta sem eru varðveittir frá staðbundnum birgjum og þjónustuveitum. Til viðbótar við eyðublað 41 verður eyðublað 11 að vera myndað til að gefa upplýsingar um alla varðveitta skatta frá erlendum aðilum. 

Skýrslan **Staðgreiðsluskattsskýrsla** í Dynamics 365 Finance inniheldur eftirfarandi skýrslur:

- Framtalseyðublað nr. 41
- Framtalseyðublað nr. 11
    
    
## <a name="prerequisites"></a>Forkröfur
Aðalaðsetur lögaðilans verður að vera í Egyptalandi.
Á vinnusvæðinu **Eiginleikastjórnun** þarf að virkja eftirfarandi eiginleika:

   - **Altækur staðgreiðsluskattur**

Nánari upplýsingar um hvernig á að virkja eiginleika er að finna í [Yfirlit eiginleikastjórnunar.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

1. Farið í **Skattur** > **Uppsetning** > **Færibreytur** > **Færibreytur fjárhags** og í flipanum **Staðgreiðsluskattur** skal stilla **Virkja altækan staðgreiðsluskatt** á **Já**.
2. Á vinnusvæðinu **Rafræn skýrslugerð** skal flytja inn eftirfarandi snið rafrænnar skýrslugerðar úr gagnageymslunni:

    - Staðgreiðsluskattsskýrsla Excel (EG)

    > [!NOTE]
    > Sniðið hér að ofan er byggt á **Skattskýrslulíkaninu** og notar **Líkanavörpun skattskýrslu**. Þessi aukalega skilgreining er sjálfkrafa flutt inn.

Frekari upplýsingar um hvernig á að flytja inn skilgreiningar rafrænnar skýrslugerðar er að finna í [Hlaða niður skilgreiningum rafrænnar skýrslugerðar úr Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Hlaða niður skilgreiningum rafrænnar skýrslugerðar

Innleiðing framtalseyðublaða staðgreiðsluskatts fyrir Egyptaland byggir á skilgreiningum rafrænnar skýrslugerðar. Frekari upplýsingar um möguleika og hugmyndir á bak við stillanlega skýrslugerð er að finna í [Rafræn skýrslugerð](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Fyrir umhverfi framleiðslu og samþykkisprófun notanda skal fylgja leiðbeiningum í efnisatriðinu [Hlaða niður skilgreiningum rafrænnar skýrslugerðar úr Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Til að búa til staðgreiðsluskattsskýrslur í egypskum lögaðila þarf að hlaða upp eftirfarandi skilgreiningum:

- Tax declaration model.version.82.xml eða nýrri útgáfu
- Tax declaration model mapping.version.82.133.xml eða nýrri útgáfu
- WHT Declaration Excel (EG).version.82.21 eða nýrri útgáfu

Þegar búið er að hlaða niður skilgreiningum rafrænnar skýrslugerðar úr Lifecycle Services (LCS) eða altæku geymslunni skal ljúka eftirfarandi skrefum.

1. Farið á vinnusvæðið **Rafræn skýrslugerð** og veljið reitinn **Skýrsluskilgreiningar**.
1. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, skal velja **Skipta út > Hlaða úr XML-skrá**.
1. Hlaðið upp öllum skránum í þeirri röð sem þær eru birtar í fyrri upptalningum. Þegar öllum skilgreiningunum hefur verið hlaðið upp ætti skilgreiningatréð að vera til staðar í Finance.

## <a name="set-up-application-specific-parameters"></a>Setja upp færibreytur tiltekins forrits

Valkostur færibreyta tiltekins forrits gerir notendum kleift að setja á skilyrði um hvernig á að flokka og reikna skattfærslurnar í hverri línu myndaðrar skýrslu eftir því hver skilgreiningin á **vöruflokki staðgreiðsluskatts** er eða önnur skilyrði sem gefin eru upp í skilgreiningu uppflettingarinnar.

Eyðublað staðgreiðsluskatts nr 41 inniheldur ákveðinn dálk þar sem staðgreiðsluskattsfærslan verður að vera flokkuð í samræmi við flokkun skattyfirvala sem heitir **Gerð afsláttarkóða**. Í stað þess að taka þessar nýju flokkanir sem ný innsláttargögn þegar færslurnar eru bókaðar munu flokkanirnar verða ákvarðaðar samkvæmt mismunandi uppflettingum sem kynntar eru í **Skilgreiningar** > **Setja upp færibreytur tiltekins forrits** > **Uppsetning** til að uppfylla kröfur staðgreiðsluskýrslna fyrir Egyptaland. 

Eftirfarandi skilgreining er notuð til að flokka færslurnar í skýrslu staðgreiðslueyðublaðs 41:

- **DiscountTaxTypeLookup**-> dálkur nr 18 

Ljúkið eftirfarandi skrefum til að setja upp mismunandi uppflettingar sem notaðar eru til að mynda staðgreiðsluskattsskýrslu og tengdar skýrslur bóka. 

1. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar** > **Uppsetning** til að setja upp reglurnar til að gera grein fyrir hvernig færslur eru flokkaðar í staðgreiðsluskattsskýrslum. 
2. Veljið núverandi útgáfu og í flýtiflipanum **Uppflettingar** skal velja heiti uppflettingar. Til dæmis **DiscountTaxTypeLookup**. Þessi uppfletting auðkennir lista yfir afsláttargerðir sem skattyfirvöld krefjast.
3. Í flýtiflipanum **Skilyrði** skal velja **Bæta við** og í nýju línunni í dálknum **Niðurstaða uppflettingar** skal velja tengda línu sem stendur fyrir flokkunina í **Dálki 18**.
4. Í dálknum **Vöruflokkur staðgreiðsluskatts** skal velja viðeigandi kóða sem er notaður til að auðkenna flokkunina. Til dæmis **Leyfður afsláttur**.  
5. Endurtakið skref 3 og 4 fyrir tiltækar uppflettingar.
6. Veljið aftur **Bæta við** til að taka með síðustu færslulínuna og í dálknum **Niðurstaða uppflettingar** skal velja **Á ekki við**. 
7. Í dálkunum sem eftir eru skal velja **Ekki autt**. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Setja upp færibreytur fyrir Fjárhag

Til að mynda skýrslur VSK-framtalseyðublaðs í Microsoft Excel skal skilgreina snið rafrænnar skýrslugerðar á síðunni **Færibreytur fjárhags**.

1. Farið í **Skattur** > **Uppsetning** > **Færibreytur fjárhags**.
2. Í flipanum **Staðgreiðsluskattur**, í reitnum **Vörpun skýrslusniðs fyrir staðgreiðsluskatt**, skal velja **Staðgreiðsluskattsskýrsla Excel (EG)**. Ef reiturinn er skilinn eftir auður verður stöðluð VSK-skýrsla búin til á SSRS-sniði.


![Framtalseyðublað](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>Mynda eyðublöð staðgreiðsluskýrslu
Ferlið við að undirbúa og senda inn eyðublað staðgreiðsluskýrslu fyrir tiltekið tímabil er byggt á staðgreiðsluskattsfærslum sem bókaðar eru við uppgjörs- og bókunarvinnu skattgreiðslu. Frekari upplýsingar um altækan staðgreiðsluskatt er að finna í [Altækur staðgreiðsluskattur](../general-ledger/global-withholding-tax-overview.md).

Ljúkið eftirfarandi skrefum til að mynda skattskýrsluna.

1. Farið í **Skattur** > **Skattframtöl** > **Staðgreiðsluskattur** > **Greiðsla staðgreiðsluskatts*.
2. Veljið jöfnunartímabilið og veljið síðan upphafsdagsetningu fyrir skýrsluna. 
3. Færið inn færsludagsetningu og veljið svo **Í lagi**.
4. Í svarglugganum sem opnast skal velja eina eða fleiri gerðir eyðublaðs **Eyðublað nr. 41**, **Eyðublað nr. 11**, eða **Ekkert**. Ef **Ekkert** er valið mun stöðluð skýrsla vera búin til. 
5. Veljið tungumálið. Allar skýrslur eru þýddar á **en-us** og **ar-eg**.
6. Færið inn útibú og heiti bankans þar sem skattgreiðslan verður innt af hendi.
7. Veljið tegund viðskipta og sláið svo inn ávísun og skjalanúmer. 
8. Færið inn einingagerðina. 
9. Færið inn heiti einstaklingsins sem skráður er fyrir því að úthluta eyðublaðinu og veljið **Í lagi** til að staðfesta myndun skýrslunnar. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
