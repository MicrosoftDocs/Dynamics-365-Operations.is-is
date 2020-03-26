---
title: Skilgreindu tölvupóststillingar í Attract
description: Þetta efni útskýrir hvernig á að skilgreina stillingar fyrir tölvupóst sem er sendur af Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: e641e3f0d1873d91be1a1dc9bc22eb734a2b21d5
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124728"
---
# <a name="configure-email-settings-in-attract"></a>Skilgreindu tölvupóststillingar í Attract

[!include [banner](includes/banner.md)]

Vörumerki þitt kemur á trausti og hjálpar þér að byggja upp samband við umsækjendur áður en þeir sækja um stöður hjá þér. Jákvæð upplifun á vörumerki laðar hæfileikaríkt fólk að og eykur hollustu núverandi starfsmanna. Microsoft Dynamics 365 Talent: Attract gerir þér kleift að skilgreina tölvupóst svo að hann endurspegli vörumerki fyrirtækisins. Þess vegna er hægt að veita samræmda upplifun starfsumsækjenda þegar þeir fara fram í gegnum umsóknarferlið.

Attract gerir þér kleift að framkvæma þessar aðgerðir:

- Skilgreindu tölvupóststillingar þannig að fyrirtækjareikningur hjá tölvupóstþjónustu Microsoft Exchange sé notaður. Þannig vita umsækjendur að tölvupósturinn kemur frá fyrirtækinu þínu. Til dæmis geturðu skilgreint stillingarnar þannig að umsækjendur fá tölvupósta frá `recruiting@contoso.com` í staðinn fyrir `contoso@microsoft.com`.
- Búðu til samræmd vörumerki fyrir öll tölvupóstssamskipti þín með því að setja altæka hausinn og fótinn fyrir tölvupóstsniðmát. 

> [!NOTE]
> Til að skilgreina Attract þannig að það noti fyrirtækjareikning tölvupóstþjónustunnar til að senda tölvupóst þarftu að nota viðbótina Alhliða ráðningar.

## <a name="connect-an-email-service-account"></a>Tengja tölvupóstþjónustureikning

Með því að tengja tölvupóstþjónustureikning við fyrirtækið þitt geturðu búið til vörumerkta tölvupóstupplifun fyrir starfsumsækjendur. Ef þú tengir fyrirtækjareikninginn þinn ekki notar Attract sjálfgefna tölvupóstsþjónustu Microsoft.

1. Veldu **Stillingar** (gírtáknið efst í hægra horni síðunnar) og veldu síðan **Stjórnandamiðstöð**.
2. Á flipanum **Tölvupóstsstillingar**, undir **Tölvupóstsþjónustureikningar**, skaltu velja **Tengja fyrirtækjareikning**.

    ![Tengi póstþjónustu fyrirtækisins í Attract](./media/attract-admin-email-service-accounts.png)

    Nánari upplýsingar um hvernig á að búa til sameiginlegan tölvupóstreikning er að finna í [Sameiginlegum pósthólfum í Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).

3. Í innskráningarglugganum í Microsoft skaltu skrá þig inn með því að nota persónuskilríki fyrirtækisins.
4. Ef þú hefur ekki enn sett upp þjónustureikning fyrir tölvupóst eða ef þú vilt bæta nýjum við skaltu velja **Bæta við nýjum þjónustureikningi** og slá síðan netfangið þitt inn. Ef þú hefur þegar sett upp þjónustureikning fyrir tölvupóst sem þú vilt nota skaltu velja hann.

Þegar póstþjónustureikningurinn þinn hefur verið skilgreindur sérðu hann skráðan undir **Póstþjónustureikningar**.

## <a name="disconnect-an-email-service-account"></a>Aftengja póstþjónustureikning

Ef þú vilt hætta að nota lén fyrirtækisins í tölvupóstsamskiptum gegnum Attract er hægt að aftengja póstþjónustureikning.

1. Veldu **Stillingar** (gírtáknið efst í hægra horni síðunnar) og veldu síðan **Stjórnandamiðstöð**.
2. Á flipanum **Tölvupóststillingar**, undir **Póstþjónustureikningar**, skaltu velja hnappinn **Meira** (þrír lóðréttir punktar) við hliðina á póstþjónustureikningnum sem þú vilt aftengja.
3. Veldu **Aftengja tölvupóstreikning**.

    ![Aftengi póstþjónustureikning fyrirtækisins](./media/attract-admin-disconnect-email-account.png)

4. Þegar þú færð kvaðningu um að staðfesta aðgerðina skaltu velja **Aftengja**.

    ![Staðfesti aftengingu á póstþjónustureikningi fyrirtækisins](./media/attract-admin-email-confirm-disconnect.png)

Ef þú tengir ekki annan tölvupóstþjónustureikning munu tölvupóstar sem eru sendir úr Attract nota sjálfgefinn tölvupóstreikning fyrir Microsoft.

## <a name="configure-email-template-settings"></a>Sskilgreindu sniðmátsstillingar tölvupósts

Þú getur hlaðið inn mynd af merki fyrirtækisins og öðrum upplýsingum sem vörumerkjahaus fyrir tölvupóstinn þinn. Þú getur einnig veitt tengla á persónuverndarstefnu og notkunarskilmála í síðufæti í tölvupósti.

> [!NOTE]
> Þú verður að fylgja öllum gildandi lögum í landi þínu eða landsvæði og einnig þess lands eða landsvæðis sem gilda um viðtakanda tölvupóstsins. Þessi lög fela í sér reglur um ruslpóst.

1. Veldu **Stillingar** (gírtáknið efst í hægra horni síðunnar) og veldu síðan **Stjórnandamiðstöð**.
2. Á flipanum **Tölvupóststillingar** undir **Stillingar fyrir sniðmát tölvupósts** skaltu draga myndina sem þú vilt nota sem tölvupósthaus inn í myndareitinn eða smella í myndareitinn til að leita að skránni. Til að skipta um núverandi mynd verðurðu fyrst að velja **Fjarlægja** við hliðina á henni. Myndin verður að vera JPEG, JPG, PNG eða SVG-skrá. Ráðlögð myndastærð er á milli 25 og 800 dílar á breidd og á bilinu 25 til 150 dílar á hæð. Hámarksskráarstærð fyrir hausinn er 1 megabæti (MB).

    ![Bætir við mynd fyrir tölvupósthöfuð fyrirtækisins](./media/attract-admin-email-header.png)

3. Undir **Persónuverndarstefna vegna samskipta** gefurðu upp tengil á persónuverndarstefnu fyrirtækisins. Undir **Skilmálar vegna samskipta** gefurðu upp tengil á notkunarskilmála fyrirtækisins.

    ![Bætir tenglum við persónuverndarstefnu fyrirtækisins og notkunarskilmála fyrir síðufót í tölvupósti](./media/attract-admin-email-footer.png)

4. Veldu **Vista** til að vista stillingar tölvupóstsniðmátsins.
