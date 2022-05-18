---
title: Slá inn hæfni
description: Starfsfólk og stjórnendur geta skráð hæfni í Dynamics 365 Human Resources.
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 32f08fa45c023c587d89623a12f101f50ef4a5fb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693004"
---
# <a name="enter-skills"></a>Slá inn hæfni

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Hægt er að færa hæfni eða raunverulega hæfni fyrir starfsmenn, umsækjendur eða tengiliði í Dynamics 365 Human Resources. Markhæfni er hæfni sem einstaklingur ætlar að ná. Raunveruleg kunnátta er kunnátta sem einstaklingur býr þegar yfir.

## <a name="create-a-workflow-to-auto-approve-skills"></a>Verkflæði stofnað til að samþykkja hæfni sjálfkrafa

Til að slá inn færni án þess að þurfa samþykki þarf að stofna verkflæði til að samþykkja færni sjálfkrafa.

> [!NOTE]
> Hæfni sem starfsmenn færa inn þurfa alltaf samþykki stjórnanda. Þetta verkflæði samþykkir aðeins hæfni sjálfkrafa sem stjórnendur færa inn fyrir hönd annarra starfsmanna.

1. Á vinnusvæðinu **Starfsmannastjórnun** velur þú **Tenglar**.

2. Undir **Skipulag**, veldu **Vinnuflæði mannauðs**.

3. Veljið **Nýtt**.

4. Á svæðinu **Stofna verkflæði** skal velja **Hæfni starfsmanns**.

   [![Velja verkflæði starfsmannahæfni.](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. Í glugganum **Opna þessa skrá?** skal velja **Opna**. Þegar beðið um skal færa inn innskráningarupplýsingar.

6. Í verkflæðisritlinum skal velja verkflæðiseininguna **Samþykkja hæfni** og færa hana yfir á vinnusvæðið.

   [![Velja verkflæðiseiningu fyrir samþykkt hæfni.](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. Tengið eininguna **Hefja** við eininguna **Samþykkja hæfni 1** og tengið síðan eininguna **Samþykkja hæfni 1** við eininguna **Ljúka**. Hugsanlega þarf að fletta niður til að sjá eininguna **Ljúka**. Hægt er að draga hana nær öðrum einingum.

   [![Tengja verkflæðiseiningar.](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. Tvísmellið á verkflæðiseininguna **Samþykkja hæfni 1** og hægrismellið síðan á eininguna **Skref 1**. Hægrismellið á eininguna **Skref 1** og veljið síðan **Eiginleikar**.

9. Í glugganum **Eiginleikar** skal velja **Skilyrði** á yfirlitsstikunni vinstra megin.

10. Veljið **Keyra á þessu þrepi aðeins þegar eftirfarandi skilyrði eru í gildi**.

11. Veljið **Bæta við skilyrði**. Eftir **Hvar** skal velja **Hæfni í sjálfsafgreiðslu starfsmanns** og síðan velja **Hæfni í sjálfsafgreiðslu starfsmanns.Einstaklingur**. Eftir **er** skal velja **reit** og síðan velja **Tengsl notanda við einstakling.Einstaklingur**.

    [![Tilgreina skilyrði.](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. Veljið **Úthlutun** á yfirlitsstikunni vinstra megin.

13. Í flipanum **Úthlutunargerð** skal velja **Stigveldi**.

14. Í flipanum **Stigveldisval**, í reitnum **Gerð stigveldis:** skal velja **Stjórnendastigveldi**.

    [![Tilgreina stjórnendastigveldi.](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. Veljið **Loka**, veljið **Verkflæði** í brauðmylsnuvinnusvæðinu og veljið því næst **Vista og loka**.

Frekari upplýsingar um stofnun verkflæðis er að finna í [Yfirlit yfir verkflæðiskerfi](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).

## <a name="enter-skills-for-a-worker"></a>Slá inn hæfni starfsmanns

1. Veljið starfsmann.

2. Á aðgerðarstikunni á síðu **Starfsmanns** skal velja **Einstaklingur** og velja síðan **Hæfni**.

3. Á síðunni **Hæfni** skal ljúka eftirfarandi reitum fyrir hverja hæfni:

   - **Hæfni**: Veljið hæfni.
   - **Stigsgerð**: Veljið **Raunverulegt** fyrir hæfni sem starfsmaður býr þegar yfir eða veljið **Markmið** fyrir hæfni sem starfsmaður stefnir að.
   - **Stig**: Veljið stig fyrir hæfni starfsmanns.
   - **Dagsetning stigs**: Veljið dagsetningu í dagbókarforritinu.
   - **Prófdómari**: Veljið prófdómara af listanum ef við á. Hægt er að sía leitina.
   - **Reynsla í árum**: Færið inn reynslu í árum.
   - **Staðfest**: Ef hæfnin er staðfest skal haka við kassann.
   - **Staðfest af**: Færið inn heiti staðfestingaraðila.

4. Þegar búið er að færa inn hæfni skal velja **Vista**.

## <a name="see-also"></a>Sjá einnig

[Skilgreina hæfni](hr-develop-skills.md)<br>
[Kortleggja hæfni](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
