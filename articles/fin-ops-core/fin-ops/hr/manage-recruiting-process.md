---
title: Haga ráðningarferlum
description: Þessi grein lýsir hugtakinu sem ráðningaraðilar geta tekið til að rekja skref í ráðningarferlinu.
author: twheeloc
ms.date: 01/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ada6dfc9b227c7ae4ca873e8354d1fcc11ecbaf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910320"
---
# <a name="manage-recruiting-processes"></a>Stjórna ráðningarferlum

> [!IMPORTANT]
> Ráðningaraðgerðin í þessari grein verður kölluð ráðningarverk og einblínir á umsækjendur, umsóknir og ráðningarverk. 


Þessi skrá lýsir hugmyndinni sem ráðningaraðilar geta nota til að rekja skref í ráðningarferli, þar með talið viðleitni til að auglýsa opnar stöður og ráða umsækjendur, rekja upplýsingar um umsækjandann og umsóknina, taka viðtöl við umsækjendur og að velja einn eða fleiri umsækjendur að fylla opnar stöður í fyrirtækinu.

## <a name="overview"></a>Yfirlit

Ráðningarverk hjálpa til við að skipuleggja skref er lokið við að fylla opnar stöður í lögaðila. Umsækjandi er sá einstaklingur sem sækir um starf innan fyrirtækisins. Umsóknin er yfirlýsing umsækjanda um áhuga á að starfa hjá fyrirtækinu og gæti verið bundin ráðningarverki til að sýna áhuga á tiltekinni stöðu. Stakur umsækjandi getur haft margar umsóknir innan sama lögaðila eða í mörgum fyrirtækjum í fyrirtækinu.

## <a name="recruitment-projects"></a>Ráðningarverk

Ráðningarverk leyfa ráðningaraðilum að rekja framvindu gegn fyllingu einna eða fleiri opinna staða. Ráðningarverkið auðkennir deild og vinnslu sem eitt eða fleiri stöður eru opin fyrir. Ráðningarverk rekja einnig eftirfarandi upplýsingar um opnar stöður:

- Nákvæmur fjöldi opinna staða
- Ráðningarstjóri og annar tengiliður fyrir stöðuna
- Dagsetningin þegar tillagan var samþykkt.
- Tímamörk umsóknar
- Áætlaður upphafsdagur

Ráðningarverkið inniheldur **Starfsauglýsinguna** gildið sem notað á síðu **Sjálfsafgreiðsla starfsmanns** til að auglýsa stöðurnar. Hægt er að birta starfsmönnum stöðurnar ef ráðningarverkið hefur gildið **Starfsauglýsing**, reitinn **Birta í sjálfsafgreiðslu starfsmanns** stilltan á **Já**, **Tímamörk umsóknar** verður að vera stillt á dagsetningu í framtíðinni, og ráðningarverkið verður að hafa í **Staða verkefnis** sem **Byrjað**. Í eftirfarandi töflu er listi yfir möguleg ráðningarverk verkstöðu og lýsingu þeirra.

| Staða    | Gefur til kynna að...                                                                         |
|-----------|-----------------------------------------------------------------------------------------|
| Raðað | Ráðningarvinna er undirbúin. Ráðningar hafa ekki enn hafist fyrir þetta verk. |
| Hafin   | Umsóknir eru nú verið samþykktar fyrir á auglýstar stöður í þessu verki.                   |
| Lokið  | Allar auglýstar stöður fyrir þetta verk hafa verið fylltar.                                         |
| Hætt við  | Ráðning hefur verið afturkölluð fyrir þetta verk.                                          |

Ráðningaraðilar geta einnig skráð fyrir **Miðla** sem notaðir voru til að auglýsa stöður gegnum ytri miðla, auk þess að rekja **Þróun** gagnvart verki eða umsóknum.

## <a name="applicants"></a>Umsækjendur

Umsækjandi er sá einstaklingur sem sækir um starf í fyrirtækinu. Umsækjendur eru samnýttir á milli allra lögaðila í fyrirtækinu. Því hefur þú stóran pott af hæfileika til að leita í. Hægt er að viðhalda færni, meðmælum, og beiðnum um aðlögun og persónulegum upplýsingum fyrir umsækjendur. Þegar færsla umsækjanda er stofnuð, tengiliðafærslu fyrir umsækjanda er stofnuð í altæku aðsetursbókinni. Hægt er að nota síðuna **Umsækjandi** til að uppfæra eftirfarandi altækar aðsetursbókarupplýsingar fyrir einstaklinga sem eru umsækjendur:

- Upplýsingar um aðsetur
- Tengslaupplýsingar
- Auðkennisupplýsingar
- Upplýsingar um nafn
- Persónulegar upplýsingar

## <a name="applications"></a>Hugbúnaður

Hægt er að skrá upplýsingar úr mótteknum starfsumsóknum í skjámyndinni **Umsókn**. Umsóknin er yfirlýsing umsækjanda um áhuga á auglýstri stöðu í fyrirtækinu. Til að stofna umsókn þarf umsækjandinn að vera þegar til sem umsækjandi eða einstaklingur í kerfinu.

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

Samskiptaaðgerð forrits ákvarðar sniðmát skjals eða tölvupóstsniðmát sem notað er til að eiga samskipti við umsækjandann sem sendi inn umsóknina. Hægt er að tengja **Bókamerki umsókna** við samskiptaaðgerðir til að leyfa að gildi séu notuð af síðunum **Umsókn**, **Umsækjandi**, **Viðtal** og **Ráðningarverk** í samskiptum við umsækjendur. Með því að búa til **sniðmát fyrir tölvupóst umsóknar** fyrir samskiptaaðgerðir geturðu sent tölvupósta á fljótlegan hátt til umsækjenda sem eru með umsóknir með ákveðna samsetningu af stöðu og samskiptaaðgerð. Til dæmis er hægt að senda staðfestingarpóst á allar umsóknir sem eru gildi fyrir **Stöðu** sem er **Móttekið** og gildi fyrir **Samskiptaaðgerð** sem **Móttekið**. Þegar tölvupósturinn hefur verið sendur þarf að uppfæra sjálfkrafa stöðu umsókna.

## <a name="application-routing"></a>Leiðir umsókna

Ef nokkrir starfsmenn þurfa að skoða umsóknina er hægt að nota síðuna **Leiðir umsókna** til að stofna dreifingarlista starfsmanna svo að hægt sé að stjórna ferlinu.

## <a name="interviews"></a>Viðtöl

**Viðtöl við umsækjendur** má áætla af síðunni **Umsóknir**. Nota skal hnappinn **Senda upplýsingar um fund** til að senda dagatalsskrár með upplýsingum um áætlað viðtal við umsækjanda og tengslaupplýsingar.

## <a name="skill-mapping"></a>Hæfnisskrá

**Hæfnisskrá** og **Forstillingar hæfniskráningar** er hægt að nota til að auðkenna umsækjendur sem kunna að vera hæfir í stöðuna.

## <a name="hiring-applicants"></a>Ráðnir umsækjendur

Nota skal **Umsóknir** síðu til að ráða umsækjanda. Þegar umsækjandi er ráðinn mun umsóknarfærslan fá stöðuna **Ráðinn** og einstaklingsfærsla umsækjandans í altækri aðsetursbók er tengd við nýja skrá starfsmanns. Breytingar á upplýsingum altækrar aðsetursbókar fyrir nýja færslu starfsmanns eru einnig birtar í færslu umsækjanda. Þetta getur minnkað gagnainnfærslu ef nýr starfsmaður sækir aldrei um annað starf innan fyrirtækisins. Til að ráða starfsmanni í nýja stöðu, smellið á **Breyta stöðu** í fellilistanum **Umsóknastaða** til að hefja flutningsferlið.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
