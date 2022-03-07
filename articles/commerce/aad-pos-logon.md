---
title: Stilla Azure Active Directory-auðkenningu fyrir innskráningu sölustaðar
description: Þetta efnisatriði útskýrir hvernig skilgreina á Azure Active Directory sem auðkenningaraðferð á Microsoft Dynamics 365 Commerce sölustað.
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 9dfb0389b0ca4b2cf75ccc70f35824674e618055
ms.sourcegitcommit: dca3279a8b7cd5d0bcd4e4a3aa9938b337aa8849
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2021
ms.locfileid: "7402152"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>Stilla Azure Active Directory-auðkenningu fyrir innskráningu sölustaðar

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að stilla Azure Active Directory (Azure AD) sem auðkenningaraðferð á Microsoft Dynamics 365 Commerce sölustað.

Smásalar sem nota Dynamics 365 Commerce ásamt öðrum skýjaþjónustum Microsoft eins og Microsoft Azure, Microsoft 365 og Microsoft Teams vilja yfirleitt nota Azure AD fyrir miðstýrða stjórnun á notandaskilríkjum fyrir örugga og hnökralausa upplifun innskráningar milli forrita. Til að nota Azure AD auðkenningu fyrir Commerce á sölustað þarf fyrst að skilgreina Azure AD sem sannvottunaraðferðina í Commerce Headquarters.

## <a name="configure-pos-authentication-method"></a>Sannvottunaraðferð sölustaðar skilgreind

Fylgja skal eftirfarandi skrefum til að stilla sannvottunaraðferð sölustaðar í Commerce Headquarters.
    
1. Farið í **Smásala og viðskipti \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur** og veljið virknireglu sem á að breyta.
1. Í hlutanum **Innskráning starfsfólks sölustaðar** í flýtiflipanum **Aðgerðir** skal velja þann valkost sannvottunaraðferðar sem óskað er eftir úr fellilistanum **Sannvottunaraðferð við innskráningu**.

    **Sannvottunaraðferð við innskráningu** inniheldur þrjá valkosti:
    
    - **Kenni og aðgangsorð starfsmanns** – Þessi sjálfgefni valkostur gerir kröfu um að notendur sölustaðar slái inn kenni og aðgangsorð starfsmanns til að skrá sig inn á sölustaðinn og fá aðgang að hnekkingaraðgerð stjórnanda.
    - **Azure AD án stakrar innskráningar** - Þessi valkostur gerir kröfu um að notendur sölustaðar noti Azure AD-innskráningarupplýsingar til að skrá sig inn á sölustað og fá aðgang að hnekkingaraðgerð stjórnanda. Þegar biðlari sölustaðar er uppfærður eða opnaður aftur verður notandi sölustaðar að gefa upp Azure AD-innskráningarupplýsingar til að skrá sig inn aftur.
    - **Azure AD með stakri innskráningu** - Þegar þessi kostur er valinn geta notendur sölustaðar skráð sig inn í sölukerfi í skýinu (CPOS) með virkum Azure AD-innskráningarupplýsingum sem önnur vefforrit nota í sama vafranum eða skráð sig inn í Modern POS (MPOS) með Azure AD-innskráningarupplýsingum í gegnum Windows. Báðar aðferðirnar heimila innskráningu án þess að það þurfi að slá Azure AD inn auðkennisupplýsingar á innskráningarskján sölustaðar. Hins vegar þarf samt að skrá sig inn með Azure AD-innskráningarupplýsingum til að fá aðgang að hnekkingaraðgerð stjórnanda á sölustað.

1. Opnið **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta > Dreifingaráætlun** og keyrið vinnsluna **1070 (Stilling rásar)** til að samstilla nýjustu stillingar virknireglu í biðlurum sölustaðar.

> [!NOTE]
> - Valkostur sannvottunaraðferðarinnar **Azure AD án stakrar innskráningar** kemur í staðinn fyrir valkostinn **Azure Active Directory** í Commerce-útgáfu 10.0.18 og eldri.
> - Azure AD auðkenning krefst virkrar internettengingar og virkar ekki þegar sölustaður er ótengdur.

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Tengja Azure AD aðganga við notendur sölustaðar

Til að nota Azure AD sem sannvottunaraðferð sölustaðar þarf að tengja Azure AD-reikninga við notendur sölustaðar í Commerce Headquarters. 

Fylgið eftirfarandi skrefum til að tengja Azure AD reikninga við notendur sölustaðar í Commerce Headquarters.
    
1. Farið í **Smásala og viðskipti > Starfsmenn > Starfskraftar** og opnið skrá starfsmanns.
1. Á aðgerðasvæðinu skal velja flipann **Commerce**, því næst undir **Ytri kenni** skal velja **Tengja fyrirliggjandi kenni**. 
1. Í valmyndinni **Nota fyrirliggjandi ytra kenni** velurðu **Leita með tölvupósti**, slærð inn Azure AD-netfangið og veldu síðan **Leita**.
1. Veljið Azure AD-reikninginn sem er skilað, veljið síðan **Í lagi**.

Að loknum skilgreiningarskrefunum hér að ofan verða reitirnir **Samheiti**, **UPN** og **Ytra undirkennimerki** í flipanum **Commerce** á upplýsingasíðu starfsmannsins fylltir út.

Keyra verður vinnsluna **1060 (Starfsfólk)** í **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta > Dreifingaráætlun** til að samstilla nýjasta notanda sölustaðar og Azure AD-reikningsgögn við rásina.

> [!NOTE]
> Þegar upplýsingar starfsmanns á borð við aðgangsorð, heimild sölustaðar, tengda Azure AD-reikninga eða aðsetursbók starfsmanns eru uppfærðar í Commerce Headquarters er sérstaklega mælt með að keyra vinnsluna **1060 (Starfsfólk)** til að samstilla nýjustu upplýsingar starfsmanns við rásina. Biðlari sölustaðar getur þá sótt rétt gögn fyrir sannvottun notanda og athuganir á sannvottun.

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>Læsa afgreiðslukassa sölustaðar og skrá sig út með Azure AD-sannvottun

Eftirfarandi gerist þegar sölustaður er skilgreindur til að nota Azure AD sannvottunaraðferðina:

- Aðgerðin **Læsa afgreiðslukassa** verður ekki í boði í forriti sölustaðar. 
- Aðgerðin **Læsa sjálfkrafa** virkar á sama hátt og aðgerðin **Skrá sig út sjálfkrafa**.
- Ef notandi sölustaðar velur **Skrá út** verður hann beðinn um að skrá sig inn með Azure AD-innskráningarupplýsingum í næsta skipti sem sölustaður ræsist burtséð frá því hvort stök innskráning er virk eða ekki.

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Hnekkingaraðgerð stjórnanda með Azure AD sannvottun

Þegar sölustaður er stilltur á að nota Azure AD-sannvottun mun hnekkingaraðgerð stjórnanda opna svarglugga sem biður um Azure AD-innskráningarupplýsingar stjórnanda. Þegar innskráning stjórnanda er samþykkt verður Azure AD-innskráningarupplýsingum stjórnanda sleppt og Azure AD-innskráningarupplýsingar fyrri notanda verða notaðar fyrir næstu sölustaðaraðgerðir.

> [!NOTE]
> - Í Commerce-útgáfu 10.0.18 og eldri styður hnekkingaraðgerð stjórnanda ekki Azure AD. Starfsmannaauðkenni og aðgangsorð eru áskilin jafnvel þótt sölustaðurinn sé stilltur á að nota Azure AD sannprófunaraðferðina.
> - Þegar CPOS er notað með Safari-vafranum í Apple iOS-tæki þarf fyrst að slökkva á **Loka á sprettiglugga** í stillingum Safari þannig að hnekkingaraðgerð stjórnanda virki með Azure AD-sannvottun. 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>Bestu starfsvenjur um öryggi varðandi Azure AD staðfestingu á deildum tækjum

Margir smásalar setja upp umhverfi smásöluverslunar sinnar á þann hátt að margir notendur þurfi að opna forrit sölustaðar úr sameiginlegu tæki. Í því samhengi, þótt stök innskráning bjóði upp á þægilega og hnökralausa upplifun sannvottunar, getur hún einnig skapað öryggisgloppu þar sem núverandi notandi sölustaðar áttar sig hugsanlega ekki á því að verið sé að nota aðrar innskráningarupplýsingar notanda til að framkvæma færslur eða aðgerðir á sölustaðnum. Áður en sölustaðurinn er stilltur á að nota Azure AD sannprófunaraðferðina er eindregið mælt með því að skoða öryggisstefnuna og innskráningarstillingar sameiginlegs tækis til að ákveða hvaða valkostur hentar best.

- Ef smásöluumhverfið þitt notar sameiginlegan reikning (til dæmis staðbundinn reikning) fyrir innskráningu í tæki á staðnum, er mælt með að nota valkostinn **Azure AD án stakrar innskráningar**. Þetta tryggir að sérhver notandi sölustaðar gefi sérstaklega upp Azure AD-innskráningarupplýsingar til að skrá sig inn á sölustað.
- Ef smásöluumhverfið gerir kröfu um að starfsmenn noti eigin Azure AD-reikninga til að skrá sig inn á sölustað í tæki á staðnum, er mælt með að nota valkostinn **Azure AD án stakrar innskráningar**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina starfsmann](tasks/worker.md)

[Stofna virknireglu fyrir smásölu](retail-functionality-profile.md)


[Setja upp aukna innskráningarvirkni fyrir MPOS og Cloud POS](extended-logon.md)

[Bestu öryggisvenjur fyrir sölukerfi í skýinu í samnýttu umhverfi](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
