---
title: Nýjungar eða breytingar í Dynamics 365 Talent - Core HR (31. október 2018)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4851c62a19bb562c7f5f578aecbae99cfcdb982f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461533"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-31-2018"></a>Nýjungar eða breytingar í Dynamics 365 Talent - Core HR (31. október 2018)

**Smíði 8.1.2031**

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.

## <a name="create-links-from-talent-to-finance"></a>Búa til tengla frá Talent að Finance
Þessi nýja leiðsöguvirkni gerir þér kleift að tengja frá Talent til Finance, sem gefur þér beina leiðsögn í síður Finance. Þegar tenglar eru grunnstilltir er hægt að tilgreina heiti og hóp tengilsins, þar sem tengilinn ætti að liggja yfir í Talent og marksíðuna sem á að opnast í Finance.

#### <a name="coming-soon"></a>Væntanlegt
Svæðasamhengi verður bætt við í framtíðinni til að leyfa beina leiðsögn í samsvarandi skrár í Finance. Til dæmis getur þú notað **Tengja við reit** til að veita samhengi til að fara beint á tiltekins starfsmanns eða stöðu í Finance.

### <a name="configure-target-systems"></a>Grunnstilla markkerfi

Í Talent geta kerfisstjórar skilgreint tengla sem birtast á vinnusvæði kerfisstjórnunar. Hluti af grunnstillingunni er Finance umhverfið sem þú vilt fara til sem „mark“ tengilsins. Þú gerir þetta með því að gefa markkerfinu nafn og gefa vefslóðina á umhverfi Finance. Hér er dæmi um vefslóð Finance sem þú myndir veita: https://devax00124aos.cloud.test.dynamics.com/. Eftir að þú hefur stillt markkerfi þín, getur þú skilgreint tenglana þína.

### <a name="configure-links"></a>Samskipa tengla

Hver tengill sem er búin til mun hafa eftirfarandi upplýsingar skilgreind.

- Tengill - Heiti tengilsins, aðeins notað til auðkenningar.

- Virkja þennan tengil - Stilltu á **Já** ef þú vilt birta tengilinn til notenda Talent.

- Sýna nafn - Skilgreina nafnið sem mun birtast sem tengill við Finance. Þessi gögn eru ekki þýdd eins og stendur.

- Birta tengil á skjámynd - Veldu hvaða síðu þú vilt birta tengilinn á.

- Hópur - Hópa er ekki krafist, en ef þú vilt skipuleggja tengla þína með hópum skaltu velja núverandi hóp eða búa til nýjan með því að nota **Hópur** reitinn.

- Markkerfi - Veldu markkerfi sem var búið til með því að nota **Stilla markkkerfi** valkost. Þetta verður umhverfi Finance sem verður notað þegar vafrað er með því að nota tengilinn.

- Notaðu núverandi fyrirtæki notanda - Veldu **Já** ef þú vilt nota samhengi núverandi fyrirtækis notandans þegar þú vafrar í Finance. Ef **Nei** er valið geturðu valið fyrirtækið sem á að nota.

- Markvalmyndaratriði - Sláðu inn valmyndaratriðið úr Finance sem tengilinn ætti að nota þegar þú vafrar. Valmyndaratriði sem þú getur farið beint á til eru tiltæk. Til að finna valmyndaratriðið sem þarf, opnaðu Finance og opnaðu síðuna sem er mark leiðsagnarinnar. Afritaðu valmyndaratriðið úr vefslóðinni. Til dæmis, ef þú vilt að tengilinn fari með þig á starfsmannalistann í Finance and Operations skaltu slá inn gildið sem birtist eftir "& mi" í vefslóðinni. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Valmyndaratriðið til að vafra um listasíðu starfsmannsins í þessu dæmi er: HcmWorkerListPage_Employees.

- Tengill við gagnaveitu - Veldu veitu gagnanna sem tengilinn vísar til. Algengustu veitur eins og **Starfskraftur** og **Staða** eru tiltækar.

- Tengill í svæði - (væntanlegt á næstunni) Val á þessu svæði leyfir að fara beint frá einni færslu Talent í staka færslu í Finance.

### <a name="access-to-links"></a>Aðgangur að tenglum

Kerfisstjórar munu sjá nýstofnaða tengla á skilgreindum síðum, jafnvel þótt **Virkja þennan tengil** valkost sé stillt á **Nei**. Þetta er hægt að nota til að prófa tengla áður en þau eru flutt til annarra starfsmanna. Öll önnur hlutverk sjá eingöngu grunnstillta tengla eftir að **Virkja þennan tengil** valkostur er stilltur á **Já**. Starfsmenn sem hafa aðgang að síðum þar sem tenglarnir birtast munu hafa aðgang að tenglum.

Notendur geta einnig haft öryggisréttindi innan Finance and Operations sem eru skilgreindar til að fá aðgang að síðum Finance and Operations. Ef það gerist ekki birtist öryggissvargluggi þegar tengilinn er notaður.


## <a name="other-changesfixes"></a>Aðrar breytingar/lagfæringar

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>Ekki er hægt að úthluta stöðum með framtíðardagsetningu til nýrrar starfsmanns

Breytingar hafa verið gerðar til að heimila úthlutanir á framtíðardagsettum stöðum til starfsmanna. Stöður sem hafa upphafsdagana í framtíðinni er hægt að velja og úthlutun til starfsmanns verður gerður þegar vinnsla er vistuð eða lokið (ef vinnuflæði er virkt).

### <a name="new-employee-cannot-be-assigned-existing-position"></a>Nýjum starfsmanni getur ekki verið úthlutað núverandi stöðu

Breytingar hafa verið gerðar þannig að ný starfsmannaverkefni geti nú verið úthlutað núverandi stöðu.

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>Starfsaldursdagsetning/Staðsetning skrifstofu hverfa þegar upphafsdagur atvinnu er í fortíðinni og skráin er vistuð

Breytingar hafa verið gerðar til að leiðrétta sýnileika **Starfsaldursdagsetningar** og **Staðsetningar skrifstofu** þegar breytingar eru gerðar á fyrri starfsmönnum.

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>Ekki er hægt að slá inn gögn fyrir framtíðardagsetta atvinnu á starfsmannasíðunni

Atvinnugögn fyrir framtíðardagsett fyrirtæki hefur verið gerður óvirkur á aðalstarfsmannasíðunni. Atvinnugögn er hægt að slá inn í gegnum **Stjórnun dagsetninga** síðurnar. Breytingar verða gerðar til viðbótar í útgáfum í framtíðinni til að hægt sé að slá inn atvinnugögn beint inn í verkflæðisferlinu.

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>Bætti ValidFrom og ValidTo við HcmPersonalContactPersonEntity

Data Management Framework (DMF) einingin HcmPersonalContactPersonEntity hefur verið uppfærð til að innihalda „gildir frá“ og „gildir til“ dagsetningar til virkja tilteknar samþættingaratburðarrásir fríðinda. 

## <a name="known-issue"></a>Þekkt vandamál
- **Vandamál**: Þegar nýtt viðhengi er bætt við starfsmann eru hnapparnir **Nýtt** og **Breyta** skyggðir. 
- **Hjáleið:** Áður en þú opnar viðhengissíðu skaltu ganga úr skugga um að FactBoxes á síðunni **Starfsmenn** séu lokaðir. Ef upplýsingareitirnir eru lokaðir þegar síðan **Starfskraftar** er hlaðið inn verða viðhengishnapparnir gerðir virkir. (Þetta vandamál verður lagað í næstu verkvangsuppfærslu.)
