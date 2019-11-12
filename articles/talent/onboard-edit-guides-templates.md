---
title: Breyta nýliðakynnngu og -sniðmátum í Dynamics 365 Talent - Onboard
description: Þetta efni útskýrir hvernig á að bæta við verkþáttum og öðrum upplýsingum við þjálfunarleiðbeiningar og sniðmát í Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0f4c68acfe021e736c259e91a40ce7d43d401246
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552003"
---
# <a name="edit-onboarding-guides-and-templates-in-dynamics-365-talent---onboard"></a>Breyta nýliðakynnngu og -sniðmátum í Dynamics 365 Talent - Onboard

[!include [banner](includes/banner.md)]

Eftir að þú hefur búið til leiðbeiningar eða sniðmát um borð í Microsoft Dynamics 365 Talent: Onboard verður þú að bæta við kynningu, verkþáttum, tengiliðum og úrræðum. Onboard gerir þér kleift að innifela ríkulegt efni í þjálfunarleiðbeiningunum þínum, þar á meðal:

- YouTube-myndbönd
- Microsoft Sway-kynningar
- Microsoft PowerApps-smáforrit
- Microsoft Stream-myndbönd
- Microsoft Forms-skjámyndir
- Iframes sem inniheldur efni á vefnum

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>Breyta kynningum eða verkþáttum sem voru fluttir inn úr sniðmáti

Ef þú býrð til þjálfunarleiðbeiningar úr sniðmáti eða ef þú flytur verkþætti úr einu sniðmáti yfir í annað, muntu taka eftir hnappnum **Læsa** á innfluttum verkþáttum. Þetta er kallað *stjórnaðir verkþættir*.

[![Stjórnaðir verkþættir](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

Þegar þú velur stýrðan verkþátt geturðu séð upprunasniðmátið efst í verkþættinum.

[![Stýrður verkþáttaruppruni](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

Ef þú breytir verkþætti í sniðmáti mun Onboard senda breytingarnar á öll sniðmátum og ósendar leiðbeiningar sem byggjast á því sniðmáti. Ef þú velur ósendar leiðbeiningar úr sniðmáti sem þú breyttir og velur síðan flipann **Starfsemi** í leiðbeiningunum muntu sjá tilkynningu um að leiðbeiningunum hafi verið breytt. Til að hafna tilkynningunni velurðu **Í lagi**. 

[![Breyta tilkynningu](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

Þú munt sjá svartan punkt við hliðina á uppfærðum verkþáttum.

[![Breytur verkþáttur](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

Þú getur ekki breytt stýrðum aðgerðum utan upphaflega sniðmátsins nema til að bæta við viðtakanda, gjalddaga eða öðrum upplýsingum í hægri hluta verkþáttarins.

Ef þú vilt breyta stýrðum verkþætti, eða ef þú vilt ekki að verkþáttur fái uppfærslur úr sniðmátinu sem hann kom úr skaltu velja hnappinn **Læsa** fyrir þann verkþátt. Hnappurinn **Læsa** mun hverfa. Verkþættinum verður ekki lengur stjórnað af upprunalega sniðmátinu og hann mun ekki lengur fá uppfærslur úr því sniðmáti. Uppfærslur sem þú gerir á verkþætti hafa ekki áhrif á upphaflega sniðmátið.

Ef þú eyðir verkþætti úr leiðbeiningum og sendir breytingar úr því sniðmáti leiðbeininganna verður verkþættinum áfram eytt í leiðbeiningunum.

> [!NOTE]
> Sniðmátum er ekki stjórnað af tengiliðum og tilföngum. Að auki er hlutum ekki stjórnað, þannig að ef þú bætir við eða breytir hluta í sniðmáti verða breytingarnar ekki sendar á neinar leiðbeiningar eða sniðmát sem nota það sniðmát.
> 
> Ef þú bætir nýjum verkþáttum við sniðmát eru nýju verkþættirnir sendir í leiðbeiningar og sniðmát sem byggjast á því sniðmáti og nýju verkþættirnir birtast efst.

## <a name="import-activities-from-another-template"></a>Flytja inn verkþætti úr öðru sniðmáti

Þú getur flutt inn verkþætti úr einu eða fleiri sniðmátum í leiðbeiningar eða sniðmát.

1. Velja skal leiðbeiningarnar eða sniðmátið sem á að breyta.

2. Veldu flipann **Verkþættir**.

3. Veldu flipann **Flytja inn** í hlutanum til hægri.

   [![Flytja inn verkþætti](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. Til að forskoða verkefnin á nýjum flipa í vafranum þínum skaltu velja hnappinn **Opna í nýjum flipa** á hvaða sniðmát sem er.

   [![Flytja inn verkþætti](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. Dragðu og slepptu viðeigandi sniðmáti á þann stað í leiðbeiningasniðmátinu sem þú vilt að verkþættirnir birtist. Haltu áfram að breyta leiðbeiningunum eða sniðmátinu.

Innfluttar aðgerðir innihalda hnappinn **Læsa**, sem gefur til kynna að þessum aðgerðum sé stjórnað af sniðmátinu sem þú fluttir inn úr. Þegar þú gerir breytingar á sniðmátinu sem þú fluttir inn uppfærast þessir verkþættir í sniðmátinu sem þú fluttir inn í þá. Breytingarnar verða þó ekki sendar sjálfkrafa í neinar leiðbeiningar sem eru búnar til úr sniðmátinu sem þú fluttir inn í.

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>Sendu breytingar úr sniðmáti yfir í önnur sniðmát eða leiðbeiningar

Ef þú breytir sniðmáti sem inniheldur verkþætti sem notaðir eru í öðrum sniðmátum eða leiðbeiningum verðurðu að senda breytingarnar ef þú vilt að þær birtist í hinum sniðmátunum eða leiðbeiningunum.

Ef þú ert ekki viss um hvort verkþættir sniðmátsins séu notaðir í öðrum sniðmátum eða leiðbeiningum skaltu velja flipann **Notað í** til að skoða hvar þessir verkþættir birtast.

   [![Skoðaðar leiðbeiningar og sniðmát eru notuð í](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

Til að senda breytingarnar þínar:

1. Vistaðu breytingarnar þínar með því að velja hnappinn **Vista**. Ef þú gerir það ekki færðu kvaðninguu m að vista breytingarnar þínar í næsta skrefi.

2. Veldu **Senda þessar breytingar**.

   
## <a name="add-or-edit-an-introduction"></a>Bættu við eða breyttu kynningu

1. Á flipanum **Kynning** slærðu inn titil fyrir leiðbeiningarnar og opnunarskilaboð. Veldu til að nota sýnishornatexta **Nota þessi skilaboð**.

    [![Inngangsflipi í Onboard-sniðmáti](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. Notaðu sniðhnappana til að kalla fram texta eins og þú vilt eða til að bæta við myndum eða tenglum.
3. Veldu **Vista** til að vista vinnuna.

## <a name="add-or-edit-activities"></a>Bæta við eða breyta verkþáttum

1. Á flipanum **Verkþættir** skaltu draga hluti frá hægri yfir á klippusvæðið.
2. Dragðu hnappinn til að skipuleggja leiðbeiningarnar í hluta skaltu draga liðinn **Nýr hluti** yfir á klippusvæðið og slá inn heiti og valfrjálsa lýsingu fyrir hlutann.

    ![[Nýjum hluta bætt við þjálfunarleiðbeiningar eða -sniðmát](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. Til að bæta verkþáttum við svo að nýliðar geti lokið þeim skaltu draga liðinn **Nýr verkþáttur** yfir á klippusvæðið og slá inn nafn og lýsingu fyrir verkþáttinn.

    ![[Nýjum verkþætti bætt við þjálfunarleiðbeiningar eða -sniðmát](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. Bæta ríkulegu efni við þjálfunarleiðbeiningarnar:

    - Til að bæta myndbandi við á YouTube skaltu draga **YouTube** liðinn yfir á klippusvæðið, slá inn heiti og lýsingu á verkþættinum og slá inn slóðina fyrir YouTube myndbandið.
    - Til að bæta við Sway-kynningu eða -fréttabréfi dregurðu **Sway**-liðinn yfir á klippusvæðið, slærð inn heiti og lýsingu á verkþættinum og slærð inn ívafna slóð fyrir Sway-kynninguna eða -fréttabréfið.
    - Til að bæta við PowerApps-forriti skaltu draga **PowerApps**-liðinn yfir á klippusvæðið, slá inn heiti og lýsingu á verkþættinum og annaðhvort velja PowerApps-forritið eða slá inn PowerApps-forritsauðkenni.
    - Til að bæta myndbandi við á Microsoft Stream skaltu draga **Microsoft Stream** liðinn yfir á klippusvæðið, slá inn heiti og lýsingu á verkþættinum og slá inn slóðina fyrir Microsoft Stream myndbandið.
    - Til að bæta við Microsoft Forms-skjámynd skaltu draga **Microsoft Forms**-liðinn yfir á klippusvæðið, slá inn heiti og lýsingu á verkþættinum, slá inn slóðina fyrir Microsoft Forms-skjámyndina og tilgreina stærð skjásvæðisins.
    - Til að bæta við iframe sem inniheldur vefefni skaltu draga liðinn **Vefefni (iframe)** yfir á klippusvæðið, slá inn heiti og lýsingu á verkþættinum, slá inn slóðina fyrir Microsoft Forms-skjámyndina og tilgreina stærð skjásvæðisins.

    ![[Nýju ríkulegu efni bætt við þjálfunarleiðbeiningar eða -sniðmát](./media/onboard-edit-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. Valfrjálst: Á svæðinu hægra megin við hvern verkþátt skal úthluta verkþættinum á ákveðinn aðila eða hlutverk, bæta við gjalddaga og tengilið og úthluta lit á flokkinn. Þegar þú úthlutar verkþætti á annan einstakling eða hlutverk er verkefni stofnað fyrir hvern einstakling. Þetta verkefni birtist á valmyndinni **Verk** í Onboard.

    [![Úthlutun verkþátta í þjálfunarleiðbeiningum eða -sniðmáti](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. Veldu **Vista** til að vista vinnuna.

Til að eyða verkþætti eða hluta velurðu hnappinn **Eyða** (ruslatunnutáknið) í efra hægra horninu í verkþættinum eða hlutanum.

Dragðu þær á nýjan stað til að endurraða verkþáttum og hlutum.

## <a name="add-or-edit-contacts"></a>Bæta við eða breyta tengiliðum

Hægt er að bæta við tengiliðum sem geta aðstoðað nýliða þína við að ná árangri frá fyrsta degi. Þessir tengiliðir geta verið ráðningaraðilar, teymisfélagar, félagar í starfsþjálfun, leiðbeinendur, kerfisstjórar og starfsfólk upplýsingatækni.

1. Á flipanum **Tengiliðir** velurðu **Nýr tengiliður**.
2. Í valmyndinni **Bæta hópmeðlimi við** slærðu inn nafn tengiliðar eða netfang, slærð inn stutta lýsingu sem útskýrir hvernig tengiliðurinn getur hjálpað nýliðanum og velur síðan **Bæta við**. 

    ![[Tengiliðum bætt við í þjálfunarleiðbeiningum eða -sniðmáti](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    Einnig er hægt að velja einn eða fleiri tengiliði undir **Tillögum**.

3. Veldu **Vista** til að vista vinnuna.

Til að eyða tengilið velurðu hnappinn **Eyða** (ruslatunnutáknið) til hægri við tengiliðinn.

Til að breyta tengilið velurðu hnappinn **Breyta** (blýantstáknið) til hægri við tengiliðinn.

## <a name="add-or-edit-resources"></a>Bæta við eða breyta tilföngum

Þú getur bætt við gagnlegum skrám, kortum og tenglum í hlutann **Tilföng** í þjálfunarleiðbeiningunum.

1. Á flipanum **Tilföng** velurðu **Nýtt tilfang**.
2. Fylgið einu af eftirfarandi skrefum:

    - Til að bæta við skrá velurðu flipann **Skrá** og dregur skrána inn á afmarkað svæði. (Að öðrum kosti skaltu smella einhvers staðar á því svæði til að leita að skránni í tölvunni eða velja **Fletta OneDrive**.) Sláðu inn heiti fyrir skrána og veldu síðan **Bæta við**.
    - Til að bæta við tengli velurðu flipann **Tengill**, slærð inn heiti og slóð fyrir tengilinn og velur síðan **Bæta við**.
    - Til að bæta við vörpun velurðu flipann **Vörpun**, slærð inn heiti og slóð fyrir vörpunina og velur síðan **Bæta við**. Onboard mun innihalda vörpun á slóðinni sem þú tilgreinir.

    ![[Tilföngum bætt við þjálfunarleiðbeiningar eða -sniðmát](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. Veldu **Vista** til að vista vinnuna.

Til að eyða tilfangi velurðu hnappinn **Eyða** (ruslatunnutáknið) til hægri við tilfangið.

Til að breyta tengilið velurðu hnappinn **Breyta** (blýantstáknið) til hægri við tilfangið.

## <a name="next-steps"></a>Næstu skref

- [Deildu efni með öðrum þátttakendum](./onboard-share-template.md)
- [Skoða stöðu verkefna og nýja starfsmenn](./onboard-view-status.md)
- [Stofna ráðningarteymi í Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Sjá einnig

- [Prófaðu eða keyptu Onboard-forritið](https://dynamics.microsoft.com/talent/onboard/)
- [Nýjungar](./whats-new.md)
- [Athugasemdir við útgáfu](https://docs.microsoft.com/business-applications-release-notes/index)
- [Fá aðstoð](./talent-support.md)
