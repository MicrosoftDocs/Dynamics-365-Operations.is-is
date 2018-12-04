---
title: "Samþætting fjárhags fyrir smásölurás"
description: "Þetta efnisatriði gefur yfirlit yfir fjárhagssamþættingu Retail POS."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: is-is
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a>Samþætting fjárhags fyrir smásölurás

[!include [banner](../includes/banner.md)]

Þetta efnisatriði er yfirlit fjárhagssamþættingarvirkni sem er að finna í Microsoft Dynamics 365 for Retail. Fjárhagssamþættingarvirkni eru rammar sem ætlað er að styðja við staðbundin lög um fjárhag sem miða að því að koma í veg fyrir svik í smásöluiðnaði. Dæmigerðar aðstæður sem fjárhagssamþætting getur náð til eru:

- Prentun fjárhagskvittunar og afhending hennar til viðskiptavinar.
- Tryggja skil á upplýsingum sem tengjast sölu og skilum sem fram fer á POS til ytri þjónustu sem stjórnvaldið veitir.
- Notkun gagnaverndar með stafrænu undirskrifti sem stjórnvald heimilar.

Þetta efnisatriði veitir leiðbeiningar um uppbyggingu fjárhagssamþættingar þannig að notendur geti sinnt eftirfarandi verkefnum. 

- Grunnstilla fjárhagstengla, sem eru fjárhagstæki eða þjónusta notuð til fjárhagsskráningar svo sem vistun, stafrænar undirskriftir og örugg skil á fjárhagsgögnum.
- Grunnstilla skjalsveitu, sem skilgreinir úttaksaðgerð og reiknirit til myndunar á fjárhagsskjali.
- Grunnstilla skráningarferli fjárhagsins, sem er skilgreint af röð skrefa og hópi tengla sem notaðar eru í hverju skrefi.
- Úthluta skráningarferlum fjárhags til POS-virknireglna.
- Úthluta tengli virknireglu, annaðhvort til vélbúnaðarsniðs (fyrir staðbundna fjárhagstengla) eða til POS-virknireglna (fyrir aðrar gerðir fjárhagstengla).

## <a name="fiscal-integration-execution-flow"></a>Framkvæmdarflæði fjárhagssamþættingar
Eftirfarandi atburðarás sýnir sameiginlegt framkvæmdarflæði fjárhagssamþættingar.

1. Frumstilling á skráningarferli fjárhagsins.
  
   Eftir að hafa gert aðgerðir þar sem fjárhagsskráningar er krafist, eins og eftir að smásöluverslun hefur verið gerður, er skráningarferli fjárhagnsins tengt núverandi POS-virknireglu.

1. Leitaðu að fjárhagstengli.
   
   Fyrir hvert þrep fjárhagsskráningar í skráningarferli fjárhagsins, stemmir kerfið saman við lista yfir fjárhagstengla. Þessir tenglar hafa virknireglu sem er innifalin í tilgreindum tenglahópi, með lista yfir tengla sem innihalda tæknilegar upplýsingar í tengslum við núverandi vélbúnaðarsnið (aðeins fyrir gerð tengils sem jafngildir **Staðbundinn**) eða með núverandi POS-virknireglu (fyrir aðrar gerðir af tenglum).
   
1. Framkvæma fjárhagssamþættingu.

   Kerfið framkvæmir allar nauðsynlegar aðgerðir sem eru skilgreindar af samsetningu sem er tengd við tengilinn sem fannst. Þetta er gert í samræmi við stillingar virknireglunnar og tæknisniðsins sem fundust í fyrra skrefi fyrir þennan tengil.

## <a name="setup-needed-before-using-fiscal-integration"></a>Uppsetning þarf áður en fjárhagssamþætting er notuð
Áður en þú notar fjárhagnssamþættingarvirknina ættirðu að skilgreina eftirfarandi stillingar:

- Skilgreindu númeraröðina á **Smásölufæribreytur** síðu fyrir númer tækniforstillingar fjárhags.
  
- Skilgreindu númeraröðin á **Smásölufæribreytur** síðu fyrir eftirfarandi tilvísanir:
  
  - Númer tækniforstillingar fjárhags
  - Flokksnúmer fjárhagstengils
  - Númer skráningarferlis

- Búðu til **Fjárhagstengil** í **Smásala> Rásaruppsetning > Fjárhagssamþætting > Fjárhagstenglar** fyrir hvert tæki eða þjónustu sem þú ætlar að nota til fjárhagssamþættingar.

-  Búa til **Fjárhagsskjalsveitu** í **Smásala> Rásaruppsetning > Fjárhagssamþætting > Fjárhagsskjalsveitur** fyrir alla fjárhagstengla. Gagnakortalagning er talin hluti af fjárhagsskjalsveitu. Til að setja upp mismunandi gagnakortalagningu fyrir sama tengilinn (eins og samkvæmt staðbundnum reglugerðum), ættir þú að búa til mismunandi fjárhagsskjalsveitur.

- Búa til **Virkniforstillingu tengils** í **Smásala> Rásaruppsetning> Fjárhagssamþætting> Virkniforstillingar tengils** fyrir hverja fjárhagsskjalsveitu.
  - Veldu heiti tengils.
  - Veldu skjalsveitu.
  - Tilgreina stillingar VSK-hlutfalls á **Uppsetningar** flipanum.
  - Tilgreina vörpun VSK-kóða og greiðslumátta á flipanum **Gagnakortalagning**.

  #### <a name="examples"></a>Dæmi 

  |  | Snið | Dæmi | 
  |--------|--------|--------|
  | Stillingar VSK-hlutfalls | gildi : VAThlutfall | 1 : 2000, 2 : 1800 |
  | Vörpun VSK-kóða | VSKkóði : gildi | vsk20: 1, vsk18: 2 |
  | Setja upp greiðslumáta | TenderTyp: gildi | Reiðufé: 1, kort: 2 |

- Búa til **Fjárhagstenglahópa** í **Smásala> Rásaruppsetning> Fjárhagssamþætting> Fjárhagstenglahópur**. Tenglahópur er hluti af virkniforstillingum sem tengjast fjárhagstenglum sem framkvæma sömu aðgerðir og eru notaðar á sama stigi innan skráningarferlis fjárhagsins.

   - Bæta virkniforstillingum við tenglahópinn. Smelltu á **Bæta við** á síðunni **Virkniforstillingar** og veldu forstillingarnúmer.
   - Ef þú vilt hætta að nota virkniforstillinguna skaltu stilla **Slökkva** á **Já**. 
   
     Þessi breyting hefur aðeins áhrif á núverandi tenglahóp. Þú getur haldið áfram að nota sömu virkniforstillingu fyrir aðra tenglahópa.

     >[!NOTE]
     > Innan tenglahópsins getur hver fjárhagstengill aðeins haft eina virkniforstillingu.

- Búa til **Tækniforstillingu tengils** í **Smásala> Rásarppsetning> Fjárhagssamþætting> Tækniforstilling tengils** fyrir hvern fjárhagstengil.
  - Veldu heiti tengils.
  - Veldu gerð tengils: 
      - **Staðbundinn** - Veldu þessa gerð fyrir tæki eða forrit sem eru settar upp á staðbundinni tölvu.
      - **Innri** - Veldu þessa gerðfyrir fjármálatæki og þjónustu sem tengist smásöluþjóni.
      - **Ytri** - Fyrir ytri fjárhagsþjónustu eins og vefgátt sem skattyfirvöld veita.
    
  - Tilgreina stillingar á **Tenging** flipanum.

      
 >[!NOTE]
 > Uppfært útgáfa af grunnstillingum sem var hlaðið áður verður hlaðinn fyrir bæði hagnýtur og tæknileg snið. Ef viðeigandi tengill eða skjalveita er þegar í notkun verður þú tilkynnt. Sjálfgefið er að allar breytingar sem hafa verið gerðar handvirkt í hagnýtum og tæknilegum sniðum verða geymdar. Til þess að hunsa þessi snið með sjálfgefnum færibreytum úr grunnstillingunni skaltu smella á **Uppfæra** á **Virkniforstillingar tengils** síðu og **Tækniforstillingar tengils** síðu.
 
- Búa til **Skráningarferli fjárhags** í **Smásala> Rásaruppsetning> Fjármálasamþætting> Skráningarferli fjárhagsins** fyrir hvert einkvæmt ferli í fjárhagssamþættingunni. Skráningarferli er skilgreint með röð skráningarskrefanna og tenglahópnum sem notaður er í hverju skrefi. 
  
  - Bæta við skráningarskrefum við ferlið:
      - Smellið á **Bæta við**.
      - Veldu gerð tengils.
      
      >[!NOTE]
      > Þetta reitur skilgreinir hvar kerfið leitar í tæknforstillingunni að tenglinum, annaðhvort í vélbúnaðarsniðum fyrir tenglategundina **Staðbundinn**, eða í POS-virknireglum fyrir aðra gerðir fjárhagstengla.
      
   - Veldu tenglahóp.
   
     >[!NOTE]
     > Smelltu á **Villuleita** til að athuga heilleika skráningarferlis uppbyggingarinnar. Mælt er með því að villuleitir séu gerðar í eftirfarandi tilvikum:
       >- Fyrir nýtt skráningarferli eftir að allar stillingar hafa verið gerðar, þ.m.t. binding við POS-virknireglur og vélbúnaðarsnið.
       >- Eftir að uppfærslur hafa verið gerðar á skráningarferli sem fyrir er.

-  Bindið skráningarferli fjárhagsins við POS-virknireglur í **Smásala> Rásaruppsetning> POS-uppsetning> POS-reglur> Virknireglur**.
   - Smelltu á **Breyta** og veldu **Númer ferlis** á **Skráningarferli fjárhagsins** flipanum.
- Tengd tækniforstillingar tengilsins við vélbúnaðarsniðin í **Smásala> Rásarstillingar > POS-uppsetning> POS-reglur> Vélbúnaðarsnið**.
   - Smelltu á **Breyta**, smelltu svo á **Nýtt** á flipanum **Tækniforstilling fjárhags**.
   - Veldu tækniforstillingu tengilsins í reitnum **Forstillingarnúmer**.
   
     >[!NOTE]
     > Þú getur bætt nokkrum tækniforstillingum við vélbúnaðarsnið. Hins vegar er þetta ekki studd ef vélbúnaðarsniðið hefur fleiri en eina skörun við hvaða tenglahóp sem er. Til að koma í veg fyrir rangar stillingar er mælt með því að þú villuleitir skráningarferlið eftir að uppfæra öll vélbúnaðarsniðin.

