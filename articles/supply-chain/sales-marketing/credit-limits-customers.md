---
title: Lánamark fyrir viðskiptavininn
description: Í þessari grein er að finna yfirlit yfir hvernig lánamark virkar í Microsoft Dynamics 365 for Finance and Operations.
author: omulvad
manager: AnnBe
ms.date: 09/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8fd7022eb1ed2671fcfc2861eb8ec7504ebf9f98
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551815"
---
# <a name="credit-limits-for-customers"></a>Lánamark fyrir viðskiptavininn

[!include [banner](../includes/banner.md)]

Með því að setja lánamark er hægt að tilgreina hámarksfjölda lána til viðskiptavina þinna. Ef lánamark er tilgreint er það kannað sjálfkrafa þegar notandi reynir að uppfæra skjal. Ef farið er yfir lánamark birtist skilaboð til notandans. Í þessari grein er að finna yfirlit yfir hvernig lánamark virkar og svör við eftirfarandi spurningum:

-   Hvaða skjöl og ferla get ég kannað lánamark fyrir?

-   Hvar skilgreini ég hvernig reikna á út annað lánsfé viðskiptavinar?

-   Hvar eru upplýsingar um notkun annars lánsfjár viðskiptavinar?

-   Hvar tilgrein ég hvort auðkenningar sé krafist til að útvíkka lán til viðskiptavinar sem og upphæð lánamarks sem krefst auðkenningar?

-   Hvar tilgreini ég hvort viðvörun eða villa birtist ef lánamarki er náð?

-   Hvernig tilgreini ég lánamark fyrir tiltekinn viðskiptamann.

-   Hvernig athuga ég lánamark handvirkt á sölupöntunum?

**Hvaða skjöl og ferla get ég kannað lánamark fyrir?**

Notaið **Færibreytur viðskiptakrafna** til að skilgreina hvaða skjöl á að kanna lánamark fyrir. Þú verður að vera meðlimur kerfisstjórnunar (-SYSADMIN-) öryggishlutverks til að gera breytingar hér. Þú getur athugað lánamörk fyrir eftirfarandi skjöl og ferli:

-   Reikningar fyrir sölupantanir þegar reikningar eru bókaðir

-   Fylgiseðlar fyrir sölupantanir þegar fylgiseðlar eru uppfærðir

-   Sölupantanir, þegar línum er bætt við á **Sölupöntun** skjámyndinni

-   Sölupantanir, þegar þær eru búnar til með þjónustu

-   Reikningar með frjálsum texta, þegar reikningar eru bókaðir

Lánamörk eru sjálfkrafa könnuð ef annaðhvort af eftirfarandi er valið:

-   Í **Færibreytur viðskiptakrafna** skjámyndinni er **Gerð lánamarks** reiturinn ekki stilltur á **Ekkert**. Lánamörk eru athuguð fyrir alla viðskiptavini.

-   Í **Færibreytur viðskiptakrafna** skjámyndinni er **Gerð lánamarks** reiturinn stilltur á **Ekkert** en **Skyldulánamark** er valið fyrir viðskiptavininn í **Viðskiptavinir**. Lánamörk eru aðeins skoðuð fyrir tiltekna viðskiptavini.

Til að athuga lánamörk fyrir eftirfarandi skjöl þarf að tilgreina viðbótarstillingar.

|    Skjal                                    |    Viðbótarstillingar                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    Reikningur með frjálsum texta                         |    Í færibreytum viðskiptakrafna, í lánamark svæðinu skal velja Kanna lánamark á reikningum með frjálsum texta.     |
|    Sölupöntun (handskráning)            |    Í færibreytum viðskiptakrafna, í lánamark svæðinu skal velja Kanna lánamark á sölupöntunum.           |
|    Sölupöntun (móttekin rafrænt)     |    Í færibreytum viðskiptakrafna, í AIF-svæðinu skal velja Kanna lánamark á sölupöntunum.                     |

**Hvar stilli ég það hvernig eftirfarandi lánamark viðskiptavinar er reiknað?**

Þú getur stillt Dynamics 365 á að reikna út eftirfarandi lánamark viðskiptavinar á einhvern eftirfarandi hátt:

-   Bera saman lánamark gagnvart stöðu viðskiptavinar..

-   Lánamark er athugað gagnvart stöðu viðskiptavinar og upphæðum fylgiseðils.

-   Lánamark er athugað gagnvart stöðu viðskiptavinar og öllum opnum færslum. Þetta inniheldur upphæðir fylgiseðla og sölupöntunar.

Notið **Færibreytur viðskiptakrafna** til að tilgreina upplýsingarnar sem á að bera saman við. Þú verður að vera meðlimur kerfisstjórnunar (-SYSADMIN-) öryggishlutverks til að gera breytingar hér. Í reitinn **Gerð lánamarks** skal velja hvort kanna eigi lánamark og hvaða færsluupplýsingar eigi að taka með þegar lánamark er athugað. Veldu úr eftirfarandi valkostum:

-   **Ekkert** – Kanna ekki lánamark. Þú getur hnekkt þessum valkosti fyrir ákveðinn viðskiptavin með því að velja reitinn **Skyldulánamark** í **Viðskiptavinir**. Ef þetta er gert er lánamark athugað gagnvart stöðu viðskiptavinar.

-   **Staða** – lánamark er athugað gagnvart staða viðskiptamanns.

-   **Staða + fylgiseðill eða innhreyfingarskjal afurða** – lánamark er athugað gagnvart stöðu viðskiptavinar og afhendingar.

-   **Staða + allt** - lánamark er athugað gagnvart staða viðskiptamanns, afhendingar og opnum pöntunum.

**Hvar eru upplýsingar um notkun annars lánsfjár viðskiptavinar?**

Upplýsingar um stöðu viðskiptavina og útistandandi lánsfjárhæð eru reiknaðar og vistaðar þegar þú býrð til skyndimynd og þær birtast í **Innheimta**. Fjárhæðirnar, sem birtast í **Innheimta**  geta ekki innihaldið alla færsluvirkni fyrr en ný skyndimynd er búin til. Nánari upplýsingar er að finna í [Skuldir og innheimtur í viðskiptakröfum](https://technet.microsoft.com/en-us/library/hh209221.aspx).

Upplýsingar um stöðu viðskiptavina og útistandandi fjárhæð eru reiknaðar þegar sölupantanir, fylgiseðlar og reikningar eru uppfærð, eftir því hvaða skjöl eru valin. Ef magn í skjalinu sem þú ert að vinna með myndi leiða til þess að farið sé yfir lánamark birtast skilaboð.

**Hvar tilgreini ég hvort auðkenningar sé krafist til að hækka lánamark viðskiptavina, og einnig lánamark sem krefst auðkenningar?**

Notaðu **Færibreytur viðskiptakrafna** til að tilgreina hvort auðkenning sé nauðsynleg og upphæð lánamarks sem krefst auðkenningar.
Þú verður að vera meðlimur kerfisstjórnunar (-SYSADMIN-) öryggishlutverks til að gera breytingar hér.

|    Svæði                                    |    lýsing                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Krefjast auðkenningar fyrir láni     |    Veljið um hvers konar auðkenningar er þörf fyrir viðskiptavini sem lögaðili þinn lánar. Sá kostur sem valinn er á þessu svæði ákvarðar hvenær og hvers konar upplýsinga er krafist á svæðinu Kennitala innan skjámyndarinnar Viðskiptavinir:        Nei – Engra opinberra skilríkja er krafist, óháð lánamörkum viðskiptavinarins.     Já – Krafist er númers skírteinis sem gefið er út af hinu opinbera eða annarra opinberra skilríkja séu lánamörk viðskiptavinarins hærri en eða jöfn núlli.     Neðri mörk – Krafist er númers skírteinis sem gefið er út af hinu opinbera eða annarra opinberra skilríkja séu lánamörk viðskiptavinarins hærri en eða jöfn þeim mörkum sem  slegin eru inn í svæðið Mörk innan þessarar skjámyndar.        |
|    Mörk                                    |    Sláið inn við hvaða lánamörk krafist er númers leyfis sem gefið er út af hinu opinbera eða annarra opinberra skilríkja viðskiptavinarins.    Til dæmis er slegið inn 2000 til að gera kröfu um að kenninúmer, til að mynda ökuskírteinisnúmer, sé fært inn fyrir viðskiptavini með lánamörk sem eru 2000 eða hærri.    Svæðið er aðeins tiltækt ef valið var Lágmark takmörkun í svæðinu Krefjast auðkenningar fyrir láni.                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Hvar tilgrein ég hvort viðvörun eða villa birtist ef lánamarki er náð?**

Notaðu **Færibreytur viðskiptakrafna** til að tilgreina hvort viðvörun eða villa birtist ef farið er yfir lánamarkið. Þessi viðvörun eða villa birtist þegar notandi slær inn eða sendir upplýsingar, eða það er innifalinn í kladda ef rafræn þjónusta er að meðhöndla skjölin. Þú verður að vera meðlimur kerfisstjórnunar (-SYSADMIN-) öryggishlutverks til að gera breytingar hér.

|    Svæði                                                               |    lýsing                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Skilaboð þegar farið er upp fyrir lánamark (í svæðinu Lánamark)     |    Veldu hvernig skilaboð um að farið sé yfir lánamark birtist notendum. Veldu úr eftirfarandi valkostum:        Villa - Villuboðin birtast. Þetta stöðvar yfirleitt virkni í gangi og leysa þarf vandamálið áður en hægt er að halda áfram.     Viðvörun – Viðvörunarskilaboð birtast en hægt er að halda áfram.                     |
|    Skilaboð þegar farið er upp fyrir lánamark (í svæðinu AIF)               |    Veljið hvernig skilaboð eru birtast í kladda þegar farið er yfir lánamark. Veldu úr eftirfarandi valkostum: Villa - Villuboð birtist í Undantekningaryfirlitinu og skjalið verður ekki unnið fyrr en leyst er úr villunni.     Viðvörun – Viðvörunarskilaboð birtast í undantekningaryfirlitinu en hægt er að halda áfram.        |

**Hvernig tilgreini ég upphæð lánamarks fyrir tiltekinn viðskiptamann?**

Notið **Viðskiptavinir** til að tilgreina lánamark fyrir tiltekinn viðskiptamann. Þú verður að vera meðlimur í öryggishlutverki sem er með Halda aðalviðskiptavini (CustCustomersMaintain) skyldu tengda við sig til að gera breytingar hér.

1.  Smellt er á **Viðskiptakröfur** \> **Algengt** \> **Viðskiptavinir** \> **Allir viðskiptavinir**. Tvísmellið á viðskiptavinalykil.

2.  Á **Viðskiptavinir** yfirlitinu í Aðgerðarrúðunni er smellt á **Breyta**.

3.  Færið inn gjaldmiðilsupphæð í **Lánamörk**. Þetta gildi verður að vera hærra en núll (0) og verður notað sem upphæð lánamarks.

4.  Ef það er krafist skal slá inn leyfisnúmer eða önnur opinber skilríki gefin út af yfirvaldi í **Kennitala** reitinn.

> [!NOTE]
> Í **Færibreytur viðskiptakrafna** er gerðin lánamark yfirleitt valin. Ef lánamarksgerðin er hins vegar stillt á **Ekkert** þarf einnig að velja **Skyldulánamark** gátreitinn í **Viðskiptavinir** til að geta kannað lánamark viðskiptavinarins og stöðu hans. Nánari upplýsingar um gerðir lánamarks er að finna í „Hvaða skjöl og aðferð get ég athugað lánamark fyrir?“ í þessu efnisatriði. 

**Hvernig athuga ég lánamark handvirkt á sölupöntunum?**

Stundum gætirðu þurft að athuga lánamark viðskiptavinar handvirkt. Til dæmis gætirðu athugað lánamark viðskiptavinar handvirkt áður en þú byrjar að slá inn sölupöntun. Hægt er að nota **Sölupöntun** til að kanna lánamark handvirkt. Þú verður að vera meðlimur í öryggishlutverki sem er með Viðhalda sölupöntun (SalesOrderMaintain) skyldu tengda við sig til að gera breytingar hér.

1.  Smellið á **Sala og markaðssetning** \> **Almennt** \> **Sölupantanir** \> **Allar sölupantanir**. Tvísmelltu á sölupöntun.

2.  Á skjámyndinni **Sölupöntun** á Aðgerðasvæðinu, á flipanum **Stjórna** skal smella á **Kanna lánamark**.
