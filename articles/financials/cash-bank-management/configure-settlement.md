---
title: "Skilgreina uppgjör"
description: "Hvernig og hvenær færslur eru gerð upp getur verið flókin viðfangsefni, svo það er mikilvægt að þú skiljir og rétt skilgreinir færibreytur til að mæta þörfum fyrirtækis þíns. Þessa efnisatrðið lýsir færibreytunum sem eru notaðar til að jafna bæði viðskiptakröfur og viðskiptaskuldir."
author: kweekley
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 66e2fdbf7038a2c15fb373d4f96cd6e6c4c87ea0
ms.openlocfilehash: 1361bce94f6542112cf29e369f2238f211d0647e
ms.contentlocale: is-is
ms.lasthandoff: 05/23/2018

---

# <a name="configure-settlement"></a>Skilgreina uppgjör

[!include [banner](../includes/banner.md)]

Hvernig og hvenær færslur eru gerð upp getur verið flókin viðfangsefni, svo það er mikilvægt að þú skiljir og rétt skilgreinir færibreytur til að mæta þörfum fyrirtækis þíns. Þessa efnisatrðið lýsir færibreytunum sem eru notaðar til að jafna bæði viðskiptakröfur og viðskiptaskuldir. 

Eftirfarandi færibreytur hafa áhrif á hvernig uppgjör eru unnin í Microsoft Dynamics 365 for Finance and Operations. Jöfnun er ferli þar sem reikningur er jafnaður gegn greiðslu eða kreditnótu. Þessar færibreytur eru staðsettar í á **uppgjör** svæði í **Færibreytur viðskiptakrafna** og **Færibreytur viðskiptaskulda** síður.

- **Sjálfvirkt uppgjör** – þessi valkostur er Stilltur **Já** ef á að jafna færsluna sjálfvirkt gagnvart öðrum opnum færslum þegar hún er bókuð. Ef þessi valkostur er stilltur á **Nei**, geta notendur handvirkt jafna færslur þegar greiðslur eru færðar inn, eða seinna með því að nota í **Jafna færslur** síðu.
- **Stýring staðgreiðsluafsláttar** – Tilgreina hvernig skal meðhöndla [staðgreiðsluafsláttar þegar reikningur ofgreiddur](cash-discount-handling-overpayments.md). Fyrir ofgreiðslu er hægt að minnka staðgreiðsluafslátt, hægt er að meðhöndla það sem mismun eða hún getur verið áfram á reikning fyrir lánardrottinn eða viðskiptavinur.
  -   **Ótilgreint** – upphæð staðgreiðsluafsláttar er dregið frá upphæð ofgreiðslan. Þessi hegðun á alltaf við, óháð hvort upphæð ofgreiðslu er yfir eða undir upphæðin sem færð er inn í á **Hámark ofgreiðslu eða vangreiðslu** svæði.
  -   **Tilgreint** Upphæð fyrir ofgreiðslu er annað hvort bókuð í fjárhagslykil mismunar fyrir staðgreiðsluafslátt eða skilið eftir stöðu á reikningi viðskiptavinar eða lánardrottins. Þessi tilgreinda Hegðun fer eftir því hvort upphæð ofgreiðslu er milli 0,00 og upphæðin sem færð er inn í á **Hámark ofgreiðslu eða vangreiðslu** svæði, eða hvort upphæð fyrir ofgreiðslu er meira en **Hámark ofgreiðslu eða vangreiðslu** upphæð.
- **Hámarks auramismunur** – Færið inn hámark leyfðs auramismunar fyrir jafnaða færslu. Ef mismunur er jafn eða minni en auramismunur sem tilgreindur er í þessu svæði verður hann bókaður á þann fjárhagslykil auramismunar sem er tilgreindur í síðunni **Lyklar fyrir sjálfvirkar færslur**.
- **Hámark ofgreiðslu eða vangreiðslu** – færið Inn upphæð sem samþykkt er fyrir ofgreiðslu og vangreiðslu. Til að reikna skatt á ofgreiðslur eða vangreiðslur skal fara á á **fjárhagsfæribreytur** síðunni er smellt á **vsk**, og því næst á **virðisaukaskatt á ofgreiðslu eða vangreiðslu** valkost.
  -   Valdi ofgreiðslan/vangreiðslan auramismun undir þeim mun sem tilgreindur er í svæðinu **hámarks auramismunur** bókast auramismunurinn í lykil auramismunar.
  -   Valdi ofgreiðslan/vangreiðslan auramismun yfir þeim mun sem tilgreindur er í svæðinu **hámarks auramismunur** bókast auramismunurinn í lykil mismunar sem er valinn fyrir **staðgreiðsluafsláttur viðskiptavinar** eða **staðgreiðsluafsláttur lánardrottins** bókunargerð á **lyklar fyrir sjálfvirkar færslur** síðunni.
- **Reikna staðgreiðsluafslætti fyrir hlutagreiðslur** – þessi valkostur er Stilltur **Já** til að virkja staðgreiðsluafslátt sem reiknast sjálfkrafa fyrir hlutagreiðslur.
  -   Áhrif þessa valkosturs fer eftir því gildi í **Nota staðgreiðsluafslátt** reit á í **Jafna færslur** síðu. Ef þessi valkostur er stilltur á **Já**, er afsláttur tekin þegar **Nota staðgreiðsluafslátt** er stillt á **Venjulegt**. Þegar **Nota staðgreiðsluafslátt** er stillt á **Alltaf**, er staðgreiðsluafsláttur alltaf tekinn, óháð stillingu þessa svæðis. Þegar **Nota staðgreiðsluafslátt** er stillt á **aldrei**, er staðgreiðsluafsláttur aldrei tekinn, óháð stillingu þessa svæðis.
  -   Ef þessi valkostur er stilltur á **já** og notandi breytir gildinu í reitnum **Upphæð til jöfnunar** á skjámyndinni **Jafna færslur** er afslátturinn sjálfkrafa reiknaður og sýndur sem sjálfgefin upphæð í reitnum Upphæð **staðgreiðsluafsláttar sem á að taka**.
  -   Ef þessi valkostur er stilltur á **nei** og notandi breytir gildinu í reitnum **Upphæð til jöfnunar** á skjámyndinni **Jafna færslur** er sjálfgefin upphæð í reitnum **Upphæð staðgreiðsluafsláttar sem á að taka** er **0**.
- **Reikna staðgreiðsluafslætti fyrir kreditnótur** – þessi valkostur er Stilltur **Já** til að sjálfkrafa reikna staðgreiðsluafslátt fyrir kreditnótur. Í viðskiptakröfum er færsla kreditnótu neikvæð færsla sem hefur gildið í reitnum **Reikningur** á **reikningur með frjálsum texta** síðu, eða bakfærsla á **sölupöntun** síðu.
  - Áhrif þessa valkosturs fer eftir því gildi í <strong>Nota staðgreiðsluafslátt</strong> reit á í <strong>Jafna færslur</strong> síðu. Ef þessi valkostur er stilltur á <strong>Já</strong> er afsláttur tekin þegar reiturinn *<strong><em>Nota staðgreiðsluafslátt</em></strong>* er stilltur á <strong>Venjulegt</strong>. Þegar reiturinn *<strong><em>Nota staðgreiðsluafslátt</em></strong>* er stilltur á <strong>Alltaf</strong> er staðgreiðsluafsláttur alltaf tekinn, óháð stillingu reitsins. Þegar reiturinn *<strong><em>Nota staðgreiðsluafslátt</em></strong>* er stilltur á <strong>Aldrei</strong> er staðgreiðsluafsláttur aldrei tekinn, óháð stillingu reitsins.
  - Ef þessi valkostur er stilltur á **já** og kreditnóta erer meerkt á **Jafna færslur** síðu er afslátturinn sjálfkrafa reiknaður og sýndur sem sjálfgefin upphæð í reitnum Upphæð **staðgreiðsluafsláttar sem á að taka**.
  - Ef þessi valkostur er stilltur á **nei** og kreditnóta er merkt á **Jafna færslur** síðu er sjálfgefin færsla í reitnum **Upphæð staðgreiðsluafsláttar sem á að taka** er **0**

- **Afsláttur mótlykla (aðeins AP)** – Tilgreina sjálfgefna staðgreiðsluafsláttur fjárhagslykils sem á að nota fyrir bókhaldsfærsla fyrir staðgreiðsluafslátt.
  -   **Nota aðallykils fyrir afslátt lánardrottins** – staðgreiðsluafslátturinn er bókaður á aðallykil sem er skilgreint í á **uppsetning staðgreiðsluafsláttar** síðu.
  -   **Lyklarnir á reikningslínum** – staðgreiðsluafslátturinn er bókaður á fjárhagslykla á upphaflega reikninginn.
- **Merkja línur í reikningur með frjálsum texta og vaxtanótum (aðeins AR)** – þessi valkostur er Stilltur **Já** til að virkja **Merkja reikningslínur** hnappinn á í **færa Inn greiðslur viðskiptavina**, **færslubókarfylgiskjal greiðslu**, og **Jafna færslur** síður. Þessi hnappur gerir notendum kleift að merkja einstakar línur fyrir jöfnun.
- **Forgangsraða jöfnun (aðeins AR)** – þessi valkostur er Stilltur **Já** til að virkja á **Merkja eftir forgangi** hnappinn á í **færa Inn greiðslur viðskiptavina** og **Jafna færslur** síður. Þessi hnappur gerir notendum kleift að úthluta fyrirframákveðinni jöfnunarröð fyrir færslur.  Eftir að jöfnunarröð hefur verið notuð í færslu, röð og úthlutun greiðslu er hægt að breyta fyrir bókun.
- **Nota forgang fyrir sjálfvirkar jafnanir** – þessi valkostur er Stilltur **Já** til að nota skilgreindan forgangsröðun þegar færslur eru jafnaðar sjálfkrafa. Þetta svæði býðst aðeins ef **Forgangsraða jöfnun** og **Sjálfvirka jöfnun** valkostir eru stillt á **Já**.

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a>Fastar víddir á aðallyklum viðskiptakrafa/viðskiptaskulda

Þegar fastar víddir eru notaðar á aðallyklum viðskiptakrafa/viðskiptaskulda, verða viðbótarbókhaldsfærslur og tvær lánardrottnafærslur í viðbót bókaðar af jöfnunarferlinu. Jöfnun ber saman fjárhagslykil viðskiptakrafa/viðskiptaskulda frá reikningi og greiðslu.  Þegar greiðsla og jöfnun er lokið saman, sem er dæmigerða atburðarásin, er bókhaldsfærsla greiðslunnar ekki bókuð í fjárhag fyrr en jöfnunarferlinu er einnig lokið. Vegna röðunar á vinnslum tilvika getur jöfnun ekki ákvarðað raunverulegan fjárhagslykil viðskiptakrafa/viðskiptaskulda út frá bókhaldsfærslu greiðslunnar. Jöfnun enduruppbyggir hvað fjárhagslykill verður fyrir greiðslu. Þetta verður að vandamáli þegar föst vídd er notuð fyrir aðallykil viðskiptakrafa/viðskiptaskulda.

Til að enduruppbyggja fjárhagslykil er aðallykill viðskiptakrafa/viðskiptaskulda sóttur frá bókunarreglunni og fjárhagsvíddirnar eru sóttar frá skrá lánardrottnafærslu fyrir greiðsluna eins og er skilgreint í greiðslubók. Fastar víddir eru ekki sjálfgefnar í greiðslubækur, en í staðinn eru þær notaðar á aðallykil sem síðasta skrefið í bókunarferlinu. Þar af leiðandi er fasta víddargildið líklega ekki í lánardrottnafærslunni nema það hafi komið að sjálfgefnu í gegnum annan uppruna á borð við lánardrottin. Enduruppbyggður lykill mun ekki innihalda föstu víddina. Vinnsla jöfnunar mun ákvarða að það verður að búa til leiðréttingarfærslu vegna þess að reikningurinn sem var bókaður með fasta víddargildinu og enduruppbyggðu greiðslunni var það ekki.  Sem jöfnunin heldur áfram með bókun leiðréttingarfærslunnar, er síðasta skrefið í bókuninni fyrir föstu víddina sem á að nota. Með því að bæta föstu víddinni við leiðréttingarfærsluna er hún bókuð með debet og kredit á sama fjárhagslykil. Jöfnun getur ekki endurheimt bókhaldsfærsluna.

Til að koma í veg fyrir fleiri bókhaldsfærslur, debet og kredit á sama fjárhagslykil, skal taka tillit til eftirfarandi úrræða, fer allt eftir þörfum fyrirtækisins. 

-   Fyrirtæki nota oft fastar víddir að núllfylla fjárhagsvídd sem er ekki krafist. Þetta er almennt raunin fyrir efnahagslykla, svo sem viðskiptakröfur/viðskiptaskuldir. Lykilskipulag er hægt að nota til að fylgjast ekki með fjárhagsvíddum sem eru venjulega núllfyllt.  Þú getur fjarlægt fjárhagsvíddina fyrir efnahagslykla sem kemur í veg fyrir nauðsyn þess að nota fasta víddir.
-   Ef fyrirtækið þitt krefst ákveðinna fastra vídda á aðallykli viðskiptakrafa/viðskiptaskulda skaltu finna leið til að gera föstu víddina sjálfgefna á greiðslunni svo að fasta víddargildið sé geymt á lánardrottnafærslunni fyrir greiðsluna. Þetta mun gera kerfinu kleift að enduruppbyggja aðallykil viðskiptakrafa/viðskiptaskulda til að hafa með föstu víddargildin. Hægt er að skilgreina fasta víddargildið sem sjálfgefið á annaðhvort lánardrottnum eða heiti færslubókar fyrir greiðslubókina.

