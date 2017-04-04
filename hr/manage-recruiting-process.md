---
title: "Stjórna ráðningarferli"
description: "Þessi skrá lýsir hugmyndinni sem ráðningaraðilar geta nota til að rekja skref í ráðningarferli, þar með talið viðleitni til að auglýsa opnar stöður og ráða umsækjendur, rekja upplýsingar um umsækjandann og umsóknina, taka viðtöl við umsækjendur og að velja einn eða fleiri umsækjendur að fylla opnar stöður í fyrirtækinu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: 551e15ed31953d6e5fc99a1177c1310194ea95d0
ms.lasthandoff: 03/31/2017


---

# <a name="manage-a-recruiting-process"></a>Stjórna ráðningarferli

Þetta efnisatriði lýsir hugmyndinni sem recruiters má nota til að rekja skref í ferli ráðningar, þar á meðal því skyni að auglýsa opnar stöður og ráðningar á umsækjendum rekja upplýsingar um umsækjandann og umsóknina, interviewing umsækjendur og því að velja einn eða fleiri umsækjendur að fylla opnar stöður í fyrirtækinu þínu.

<a name="overview"></a>Yfirlit
--------

Ráðningarverk hjálpa til við að skipuleggja skref er lokið við að fylla opnar stöður í lögaðila. Umsækjandi er sá einstaklingur sem gildir fyrir ráðningu í skal enterprise.  Umsókn umsækjanda segð vaxta sem hjá fyrirtæki í og gæti bundin ráðningarverks í flýtivísa vaxta í tilteknum opnun.  Einn umsækjandi getur haft mörg forrit innan sama lögaðila eða í mörgum fyrirtækjum í þínu fyrirtæki.

<a name="recruitment-projects"></a>Ráðningarverk
--------------------

Ráðningarverk leyfa recruiters til að rekja framvindu gagnvart einum eða fleiri opnar stöður fylla.  Ráðningarverkið auðkennir deild og vinnslu sem eitt eða fleiri stöður eru opin. Ráðningarverk rekja einnig eftirfarandi upplýsingar um opnar stöður:
-   Nákvæmur fjöldi opinna staða
-   Ráðningarstjóri og annar tengiliður fyrir stöðuna
-   Dagsetningin þegar tillagan var samþykkt.
-   Tímamörk umsóknar
-   Áætlaður upphafsdagur

Ráðningarverkið inniheldur **Starfsauglýsinguna** sem er notuð í **Sjálfsafgreiðsla starfsmanns** til að auglýsa stöðurnar. Til að birta starfsmönnum stöðurnar verður ráðningarverkið að hafa **Starfsauglýsinguna**, reitinn** Birta í sjálfsafgreiðslu starfsmanns** stilltan á Já, **Tímamörk umsóknar** verður að vera stillt á dagsetningu í framtíðinni, og ráðningarverkið verður að hafa í **staða Verks** byrjað. Í eftirfarandi töflu er listi yfir mögulegar ráðningarverk verkstöðu og lýsingu þeirra.

| **Status**    | **Indicates that…**                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| Raðað | Vinna ráðningar eru verið undirbúið.  Ráða hefur enn ekki hafist fyrir þetta verk. |
| Hafin   | Umsóknir eru nú verið samþykktar fyrir á auglýstar stöður í þessu verki.                    |
| Lokið  | Allar auglýstar stöður fyrir þetta verk hafa verið fylltar.                                          |
| Hætt við  | Ráðning hefur verið afturkölluð fyrir þetta verk.                                           |

Ráðningaraðilar geta einnig skráð fyrir **Miðla** sem notaðir voru til að auglýsa stöður gegnum ytri miðla, auk þess að rekja **Þróun** gagnvart verki eða umsóknum.

<a name="applicants"></a>Umsækjendur
----------

Umsækjandi er sá einstaklingur sem á við vinnslu í skal enterprise.  Umsækjendur eru samnýttar á milli alla lögaðila í nettenging stór hóp talent leitað frá fyrirtækinu. Hægt er að viðhalda færni, meðmælum, og beiðnum um aðlögun og persónulegum upplýsingum fyrir umsækjendur. Þegar færsla umsækjanda er stofnuð, tengiliðafærslu fyrir umsækjanda er stofnuð í altæku aðsetursbókinni. Hægt er að nota síðuna **Umsækjandi** til að uppfæra eftirfarandi altækar aðsetursbókarupplýsingar fyrir einstaklinga sem eru umsækjendur:
-   Upplýsingar um aðsetur
-   Tengslaupplýsingar
-   Auðkennisupplýsingar
-   Upplýsingar um nafn
-   Persónulegar upplýsingar

## <a name="applications"></a>Hugbúnaður
Hægt er að skrá upplýsingar úr mótteknum starfsumsóknum í skjámyndinni **Umsókn**. Forritið er umsækjandans segðina vaxta í opnun í fyrirtækinu þínu starfi.  Til að stofna umsókn er umsækjanda verður að vera þegar til sem umsækjandi eða einstaklingurinn í kerfinu.
Starfsumsóknir sem umsækjendur senda á vefnum eru annaðhvort umbeðnar umsóknir sem voru færðar inn sem svar við starfsauglýsingu eða óumbeðnar umsóknir. Umbeðnar umsóknir eru sjálfkrafa tengdar ráðningarverkinu þaðan sem auglýsingin var stofnuð. Óumbeðnar umsóknir eru tengdar ráðningarverki nu sem tilgreint er á svæðinu **Ráðningarverk** á síðunni **Færibreytur mannauðs**.
### <a name="application-status"></a>Staða umsóknar

Staða umsóknar gefur til kynna hvar umsókn er í ráðningarferlinu. Í eftirfarandi töflu er listi yfir mögulegar stöður umsókna og lýsingu þeirra.

| Staða    | Gefur til kynna að...                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Móttekið  | Dagsetningin þegar umsóknin var móttekin.                                                             |
| Staðfest | Tilkynning er send til umsækjanda til að staðfesta móttöku umsóknarinnar.            |
| Viðtal | Hægt er að senda boð um að koma í viðtal til umsækjandans.                                     |
| Höfnun | Hægt er að senda höfnunarbréf til umsækjandans.                                          |
| Hætt við  | Hægt er að senda staðfestingu um afturköllun til umsækjandans. Þessari stöðu er úthlutað handvirkt. |
| Ráðin(n)  | Hægt er að senda atvinnutilboð til umsækjandans.                                         |

### <a name="correspondence-actions"></a>Samskiptaaðgerðir

Samskiptaaðgerð **umsóknar** ákvarðar sniðmát skjals eða tölvupóstsniðmát sem notað er til að eiga samskipti við umsækjandann sem sendi inn umsóknina. Hægt er að tengja **Bókamerki umsókna** með samskiptaaðgerðir til að leyfa að nota gildi úr Forritinu, síður Umsækjanda Viðtalið og Ráðningarverk verks í þínu samskiptum við umsækjendur.  **Tölvupóstsniðmát umsókna** er hægt að stofna fyrir samskiptaaðgerðir til að senda tölvupóst fljótt til umsækjendur sem hafa forrit með tiltekna stöðu og samskipti aðgerð samsetningu. Til dæmis gæti senda Staðfestingu tölvupósts öll Forrit með í **Stöðu** móttekið og **Samskipti aðgerð** móttekið.  Eftir að senda tölvupóst, þarf að uppfæra sjálfkrafa stöðu forritin.

## <a name="application-routing"></a>Leiðir umsókna

Ef nokkrir starfsmenn þurfa að skoða umsóknina er hægt að nota síðuna **Leiðir umsókna** til að stofna dreifingarlista starfsmanna svo að hægt sé að stjórna ferlinu.

## <a name="interviews"></a>Viðtöl

**Viðtöl við umsækjendur** er hægt að raða úr á **Umsóknir** síðu.  Nota skal **Senda upplýsingar fundur** hnappinn til að senda dagatal skrá með upplýsingum röðunar viðtal við umsækjanda og tengslaupplýsingar.

## <a name="skill-mapping"></a>Hæfnisskrá

**Hæfnisskrá** og **Forstillingar hæfniskráningar** er hægt að nota til að auðkenna umsækjendur sem kunna að vera hæfir í stöðuna.

## <a name="hiring-applicants"></a>Ráðnir umsækjendur

Nota skal **Umsóknir** síðu til að ráða umsækjanda. Þegar umsækjandi er ráðinn mun umsóknarfærslan fá stöðuna **Ráðinn** og einstaklingsfærsla umsækjandans í altæka aðsetursbók er tengd við nýja færslu starfsmanns. Breytingar á upplýsingum altækrar aðsetursbókar fyrir nýja færslu starfsmanns eru einnig birtar í færslu umsækjanda. Þetta geta minnkað gagnainnfærslu ef nýjan starfsmann aldrei gildir fyrir aðra vinnslu innan fyrirtækis þíns.  Til að ráða starfsmanni í nýja stöðu, smellið á **Breyta stöðu** í á **umsóknastaða** sleppa niður hefja í ferlinu.




