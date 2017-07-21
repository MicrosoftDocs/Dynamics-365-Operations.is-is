---
title: "Stjórna ráðningarferli"
description: "Þessi skrá lýsir hugmyndinni sem ráðningaraðilar geta nota til að rekja skref í ráðningarferli, þar með talið viðleitni til að auglýsa opnar stöður og ráða umsækjendur, rekja upplýsingar um umsækjandann og umsóknina, taka viðtöl við umsækjendur og að velja einn eða fleiri umsækjendur að fylla opnar stöður í fyrirtækinu."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6276655f6e7d09f5bc8862ad456b834d8919e574
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017


---

# <a name="manage-a-recruiting-process"></a>Stjórna ráðningarferli

[!include[banner](../includes/banner.md)]


Þetta efnisatriðilýsir hugmyndinni sem ráðningaraðilar geta nota til að rekja skref í ráðningarferli, þar með talið viðleitni til að auglýsa opnar stöður og ráða umsækjendur, rekja upplýsingar um umsækjandann og umsóknina, taka viðtöl við umsækjendur og að velja einn eða fleiri umsækjendur að fylla opnar stöður í fyrirtækinu.

<a name="overview"></a>Yfirlit
--------

Ráðningarverk hjálpa til við að skipuleggja skref er lokið við að fylla opnar stöður í lögaðila. Umsækjandi er sá einstaklingur sem sækir um starf innan fyrirtækisins.  Umsóknin er yfirlýsing umsækjanda um áhuga á að starfa hjá fyrirtækinu og gæti verið bundin ráðningarverki til að sýna áhuga á tiltekinni stöðu.  Stakur umsækjandi getur haft margar umsóknir innan sama lögaðila eða í mörgum fyrirtækjum í fyrirtækinu.

<a name="recruitment-projects"></a>Ráðningarverk
--------------------

Ráðningarverk leyfa ráðningaraðilum að rekja framvindu gegn fyllingu einna eða fleiri opinna staða.  Ráðningarverkið auðkennir deild og vinnslu sem eitt eða fleiri stöður eru opin fyrir. Ráðningarverk rekja einnig eftirfarandi upplýsingar um opnar stöður:
-   Nákvæmur fjöldi opinna staða
-   Ráðningarstjóri og annar tengiliður fyrir stöðuna
-   Dagsetningin þegar tillagan var samþykkt.
-   Tímamörk umsóknar
-   Áætlaður upphafsdagur

Ráðningarverkið inniheldur **Starfsauglýsinguna** sem er notuð í **Sjálfsafgreiðsla starfsmanns** til að auglýsa stöðurnar. Til að birta starfsmönnum stöðurnar verður ráðningarverkið að hafa **Starfsauglýsinguna**, reitinn **Birta í sjálfsafgreiðslu starfsmanns** stilltan á Já, **Tímamörk umsóknar** verður að vera stillt á dagsetningu í framtíðinni, og ráðningarverkið verður að hafa í **staða Verks** byrjað. Í eftirfarandi töflu er listi yfir möguleg ráðningarverk verkstöðu og lýsingu þeirra.

| **Staða**    | **Gefur til kynna að...**                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| Raðað | Ráðningarvinna er undirbúin.  Ráðningar hafa ekki enn hafist fyrir þetta verk. |
| Hafin   | Umsóknir eru nú verið samþykktar fyrir á auglýstar stöður í þessu verki.                    |
| Lokið  | Allar auglýstar stöður fyrir þetta verk hafa verið fylltar.                                          |
| Hætt við  | Ráðning hefur verið afturkölluð fyrir þetta verk.                                           |

Ráðningaraðilar geta einnig skráð fyrir **Miðla** sem notaðir voru til að auglýsa stöður gegnum ytri miðla, auk þess að rekja **Þróun** gagnvart verki eða umsóknum.

<a name="applicants"></a>Umsækjendur
----------

Umsækjandi er sá einstaklingur sem sækir um starf í fyrirtækinu.  Umsækjendur eru samnýttar á milli allra lögaðila í samstæðunni, sem veitir stóran hóp af færu fólki til að leita í. Hægt er að viðhalda færni, meðmælum, og beiðnum um aðlögun og persónulegum upplýsingum fyrir umsækjendur. Þegar færsla umsækjanda er stofnuð, tengiliðafærslu fyrir umsækjanda er stofnuð í altæku aðsetursbókinni. Hægt er að nota síðuna **Umsækjandi** til að uppfæra eftirfarandi altækar aðsetursbókarupplýsingar fyrir einstaklinga sem eru umsækjendur:
-   Upplýsingar um aðsetur
-   Tengslaupplýsingar
-   Auðkennisupplýsingar
-   Upplýsingar um nafn
-   Persónulegar upplýsingar

## <a name="applications"></a>Hugbúnaður
Hægt er að skrá upplýsingar úr mótteknum starfsumsóknum í skjámyndinni **Umsókn**. Umsóknin er yfirlýsing umsækjanda um áhuga á auglýstri stöðu í fyrirtækinu.  Til að stofna umsókn þarf umsækjandinn að vera þegar til sem umsækjandi eða einstaklingur í kerfinu.
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

Samskiptaaðgerð **umsóknar** ákvarðar sniðmát skjals eða tölvupóstsniðmát sem notað er til að eiga samskipti við umsækjandann sem sendi inn umsóknina. Hægt er að tengja **Bókamerki umsókna** við samskiptaaðgerðir til að leyfa að gildi séu notuð af síðunum Umsókn, Umsækjandi, Viðtal og Ráðningarverk í samskiptum við umsækjendur.  Hægt er að stofna **Tölvupóstsniðmát umsókna** fyrir samskiptaaðgerðir til að senda skjótan tölvupóst til umsækjenda sem hafa umsókn með tiltekna samsetningu á stöðu og samskiptaaðgerð. Til dæmis gætirðu sent staðfestingartölvupóst til allra umsækjenda með **stöðuna** Móttekið **samskiptaaðgerðina** Móttekið.  Þegar tölvupósturinn hefur verið sendur þarf að uppfæra sjálfkrafa stöðu umsókna.

## <a name="application-routing"></a>Leiðir umsókna

Ef nokkrir starfsmenn þurfa að skoða umsóknina er hægt að nota síðuna **Leiðir umsókna** til að stofna dreifingarlista starfsmanna svo að hægt sé að stjórna ferlinu.

## <a name="interviews"></a>Viðtöl

**Viðtöl við umsækjendur** má áætla af síðunni **Umsóknir**.  Nota skal hnappinn **Senda upplýsingar um fund** til að senda dagatalsskrár með upplýsingum um áætlað viðtal við umsækjanda og tengslaupplýsingar.

## <a name="skill-mapping"></a>Hæfnisskrá

**Hæfnisskrá** og **Forstillingar hæfniskráningar** er hægt að nota til að auðkenna umsækjendur sem kunna að vera hæfir í stöðuna.

## <a name="hiring-applicants"></a>Ráðnir umsækjendur

Nota skal **Umsóknir** síðu til að ráða umsækjanda. Þegar umsækjandi er ráðinn mun umsóknarfærslan fá stöðuna **Ráðinn** og einstaklingsfærsla umsækjandans í altæka aðsetursbók er tengd við nýja færslu starfsmanns. Breytingar á upplýsingum altækrar aðsetursbókar fyrir nýja færslu starfsmanns eru einnig birtar í færslu umsækjanda. Þetta getur minnkað gagnainnfærslu ef nýr starfsmaður sækir aldrei um annað starf innan fyrirtækisins.  Til að ráða starfsmanni í nýja stöðu, smellið á **Breyta stöðu** í fellilistanum **Umsóknastaða** til að hefja flutningsferlið.






