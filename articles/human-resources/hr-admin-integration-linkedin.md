---
title: Samþætta við LinkedIn Talent Hub
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp samþættingu milli Microsoft Dynamics 365 Human Resources og LinkedIn Talent Hub.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e500125e1d96f6b595910e1168e2e1baeef0cd3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360593"
---
# <a name="integrate-with-linkedin-talent-hub"></a>Samþætta við LinkedIn Talent Hub

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) er verkvangur rakningakerfis umsækjenda (ATS). Það gerir þér kleift að finna, hafa umsjón með og ráða starfsmenn, allt á einum stað. Með því að samþætta Microsoft Dynamics 365 Human Resources við LinkedIn Talent Hub er auðveldlega hægt að stofna starfsmannafærslur í Human Resources fyrir umsækjendur sem hafa verið ráðnir í stöðu.

## <a name="setup"></a>Setja upp

Kerfisstjóri þarf að ljúka uppsetningarverkum til að virkja samþættingu við LinkedIn Talent Hub. Fyrst þarf að setja upp notanda og öryggishlutverk í Power Apps umhverfinu til að veita LinkedIn Talent Hub viðeigandi heimildir til að skrifa gögn inn í Human Resources.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Tengja umhverfið við LinkedIn Talent Hub

1. Opnaðu [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).

2. Í fellivalmynd notandans skal velja **Stillingar vöru**.

3. Á yfirlitssvæðinu vinstra megin, í hlutanum **Ítarlegt**, skal velja **Samþættingar**.

4. Veljið **Heimila** fyrir Microsoft Dynamics 365 Human Resources-samþættingu.

5. Á **Dynamics 365 Human Resources** síðunni skal velja umhverfið sem á að tengja LinkedIn Talent Hub við og síðan velja **Tengill**.

    ![Innleiðing LinkedIn Talent Hub.](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > Aðeins er hægt að tengja við umhverfi þar sem notandareikningurinn er með stjórendaaðgang að bæði umhverfi Human Resources og tengdu Power Apps-umhverfi. Ef engin umhverfi eru skráð á síðu Human Resources skal ganga úr skugga um að þú sért með heimiluð umhverfi Human Resources í leigjandanum og að notandinn sem þú skráðir inn á tengda síðu sé með stjórnendaheimildir fyrir bæði umhverfi Human Resources og Power Apps-umhverfi.

### <a name="create-a-power-apps-security-role"></a>Stofna Power Apps öryggishlutverk

1. Opna [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).

2. Í listanum **Umhverfi** skal velja umhverfið sem tengist umhverfi Human Resources sem á að tengja við tilvikið af LinkedIn Talent Hub.

3. Veldu **Stillingar**.

4. Stækkaðu hnútinn **Notendur + Heimildir** og veldu **Öryggishlutverk**.

5. Á síðunni **Öryggishlutverk**, í tækjastikunni, skal velja **Nýtt hlutverk**.

6. Í flipanum **Upplýsingar** skal færa inn heiti fyrir hlutverkið, eins og **HRIS-samþætting LinkedIn Talent Hub**.

7. Í flipanum **Sérstilling** skal velja heimildina **Lesaðgangur** á fyrirtækisstigi fyrir eftirfarandi einingar:

    - Eining
    - Svæði
    - Skyldleiki

8. Vistið og lokið öryggishlutverkinu.

### <a name="create-a-power-apps-application-user"></a>Stofna notanda fyrir Power Apps-forrit

Notandi forritsins verður að vera stofnaður fyrir breyti LinkedIn Talent Hub til að veita breytinum heimildir til að skrifa færslur umsækjanda inn í Power Apps-umhverfið.

1. Opna [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).

2. Í listanum **Umhverfi** skal velja umhverfið sem tengist umhverfi Human Resources sem á að tengja við tilvikið af LinkedIn Talent Hub.

3. Veldu **Stillingar**.

4. Stækkaðu hnútinn **Notendur + Heimildir** og veldu **Notendur**.

5. Veljið **Stjórna notendum í Dynamics 365**.

6. Notið fellivalmyndina fyrir ofan listann til að breyta yfirlitinu úr sjálfgefnu yfirliti **Virkjaðir notendur** í **Forritsnotendur**.

    ![Yfirlit forritsnotenda.](./media/hr-admin-integration-power-apps-application-users.jpg)

7. Á tækjastikunni skal velja **Nýr**.

8. Á síðunni **Nýr notandi** skal fylgja þessum skrefum:

    1. Breytið gildinu á reitnum **Gerð notanda** í **Forritsnotandi**.
    2. Stillið reitinn **Notandanafn** á **HRIS-samþætting HR LinkedIn Dynamics365**.
    3. Stilltu reitinn **Forritskenni** á **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    4. Færið inn eitthvað gildi í reitina **Fornafn**, **Eftirnafn** og **Aðalnetfang**.
    5. Á tækjastikunni skal velja **Vista \& Loka**.

### <a name="assign-a-security-role-to-the-new-user"></a>Öryggishlutverki úthlutað á nýjan notanda

Þegar búið er að vista og loka nýja forritsnotandanum í hlutanum hér að ofan er þér vísað aftur á síðuna **Listi yfir notendur**.

1. Á síðunni **Listi yfir notendur** skal breyta yfirlitinu í **Forritsnotendur**.

2. Veldu forritsnotandann sem þú stofnaðir í hlutanum hér á undan.

3. Á tækjastikunni skal velja **Stjórna hlutverkum**.

4. Veldu öryggishlutverkið sem þú stofnaðir fyrr í samþættingunni.

5. Veljið **Í lagi**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Bæta Azure Active Directory-forriti við Human Resources

1. Í Dynamics 365 Human Resources skal opna síðuna **Azure Active Directory forrit**.
2. Bættu nýrri færslu við listann og stilltu eftirfarandi reiti:

    - **Biðlarakenni**: Sláðu inn **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    - **Heiti**: Sláðu inn heiti á Power Apps öryggishlutverkinu sem þú stofnaður hér á undan, t.d. **Samþætting LinkedIn Talent Hub HRIS**.
    - **Notandakenni**: Velja skal notanda sem er með heimildir til að skrifa gögn inn í starfsmannastjórnun.

### <a name="create-the-table-in-dataverse"></a>Búa til töfluna í Dataverse

> [!IMPORTANT]
> Samþættingin við LinkedIn Talent Hub veltur á sýndartöflum í Dataverse fyrir Human Resources. Sem skilyrði fyrir þessu skrefi í uppsetningunni, verður þú að skilgreina sýndartölfur. Upplýsingar um hvernig á að skilgreina sýndartöflur er að finna í [Skilgreina Dataverse sýndartöflur](./hr-admin-integration-common-data-service-virtual-entities.md).

1. Í Human Resources skal opna síðuna **Dataverse-samþætting**.

2. Veljið flipann **Sýndartöflur**.

3. Síaðu einingalistann eftir einingarmerki til að finna **Útfluttan umsækjanda LinkedIn**.

4. Veldu eininguna og síðan **Búa til/uppfæra**.

## <a name="exporting-candidate-records"></a>Skrár umsækjanda fluttar út

Þegar uppsetningu er lokið geta ráðningaraðilar og starfsfólk mannauðs notað virknina **Flytja út HRIS** í LinkedIn Talent Hub til að flytja út færslur ráðinna umsækjenda úr LinkedIn Talent Hub í Human Resources.

### <a name="export-records-from-linkedin-talent-hub"></a>Flytja út færslur úr LinkedIn Talent Hub

Þegar umsækjandi hefur farið í gegnum ráðningarferlið og hefur verið ráðinn, geturðu flutt út skrár umsækjanda úr LinkedIn Talent Hub í Human Resources.

1. Í LinkedIn Talent Hub skal opna verkið sem þú réðst nýja starfsmanninn í.

2. Veldu skrá umsækjanda.

3. Veldu **Breyta stigi** og síðan **Ráðinn**.

4. Í úrfellingarmerki (**...**) fyrir umsækjandann skal velja **Flytja yfir í HRIS**.

5. Á svæðinu **Flytja yfir í HRIS** skal færa inn upplýsingarnar sem þarf að flytja út:

    - Í reitnum **HRIS-veitandi** skal velja **Microsoft Dynamics 365 Human Resources**.
    - Í reitnum **Upphafsdagsetning** skal velja gildi fyrir nýja starfsmanninn.
    - Í reitinn **Starfsheiti** skal færa inn starfsheiti fyrir vinnu nýja starfsmannsins.
    - Í reitinn **Staðsetning** skal færa inn staðsetninguna þar sem starfsmaðurinn verður.
    - Færðu inn eða staðfestu netfang starfsmannsins.

![Flytja yfir á HRIS-svæðið í LinkedIn Talent Hub.](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Ljúka við innleiðingu í Human Resources

Færslur umsækjanda sem eru fluttar úr LinkedIn Talent Hub í Human Resources birtast í hlutanum **Umsækjendur til að ráða** á síðunni **Starfsmannastjórnun**.

1. Í Human Resources skal opna síðuna **Starfsmannastjórnun**.

2. Í hlutanum **Umsækjendur til að ráða** skal velja **Ráða** fyrir valinn umsækjanda.

3. Í svarglugganum **Ráða nýjan starfsmann** skal fara yfir færsluna og bæta við nauðsynlegum upplýsingum. Einnig er hægt að velja staðsetningarnúmerið sem umsækjandinn hefur verið ráðinn fyrir.

Þegar búið er að færa inn nauðsynlegar upplýsingar er hægt að halda áfram með hefðbundin ferli til að búa til starfsmannafærslur og starfsmannaráðningar.

Eftirfarandi upplýsingar eru fluttar inn og teknar með í nýju starfsmannafærsluna:

- Fornafn
- Eftirnafn
- Upphafsdagur starfs
- Tölvupóstfang
- Símanúmer

## <a name="see-also"></a>Sjá einnig

[Skilgreina Dataverse-sýndartöflur](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Hvað er Microsoft Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]