---
title: Sannvottun frá þjóni til þjóns fyrir API samþættingu ATS
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp sannvottun frá þjóni til þjóns fyrir samþættingar gagnvart Dynamics 365 Human Resources API samþættingu ATS.
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ed76d22ab6b917c931220f3ba462f4f14cae207
ms.sourcegitcommit: bd684c9eb6de718573e6be5479e1832fe614d919
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/07/2021
ms.locfileid: "6373062"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>Sannvottun frá þjóni til þjóns fyrir API samþættingu ATS

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp sannvottun frá þjóni til þjóns fyrir samþættingar forrits gagnvart Dynamics 365 Human Resources API samþættingu ATS. Stjórna þarf nokkrum öryggislögum fyrir þjónustueininguna til að fá aðgang að Microsoft Dataverse sýndartöflunni og tengdum gögnum. Veita þarf notandanum aðgang að Dataverse sýndartöflunni í Microsoft Power Platform og aðgang að gögnunum í Dynamics 365 Human Resources.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Virkja aðgang að Dataverse sýndartöflum í Power Platform

Fyrsta skrefið til að virkja aðgang að Dataverse sýndartöflum í Power Platform er að setja upp forritið í Power Platform fyrir sannvottun gagnvart endastöð Dataverse sýndartöflu. Skref til að gera þetta er lýst í [Microsoft Dataverse leiðbeiningum þróunaraðila](/powerapps/developer/data-platform).

  - Fyrir skráningar á forriti með einum leigjanda: [Nota sannvottun frá þjóni til þjóns fyrir einn leigjanda](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - Fyrir skráningar á forriti með mörgum leigjendum: [Nota sannvottun frá þjóni til þjóns fyrir marga leigjendur](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>Öryggishlutverk fyrir ATS-samþættingar stofnað

Eitt af skrefunum eftir að notandi forritsins hefur verið búinn til er að úthluta notandanum öryggishlutverki sem skilgreinir þann aðgang sem forritið mun hafa að endastöðvum. Þetta er skref 7 í [Stofnun forritsnotanda](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) fyrir skráningar á forriti með einum leigjanda og [Búa til öryggishlutverk fyrir notanda forritsins](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) fyrir skráningar á mörgum leigjendum. 

Hlutverkið sem þú úthlutar forritsnotanda á að hafa aðgang að gagnaeiningum sem notaðar eru fyrir ATS-samþættinguna. Þetta er ekki til úr kassanum og því þarf að stofna nýtt öryggishlutverk. Hægt er að stofna nýja hlutverkið með því að fylgja skrefunum sem lýst er í [Búa til öryggishlutverk](/power-platform/admin/create-edit-security-role#create-a-security-role).

Fyrir nýja hlutverkið verður að úthluta viðeigandi aðgangi til að minnsta kosti eftirfarandi eininga í flipanum **Sérsniðnar einingar** í nýja hlutverkinu. Athugaðu að það gætu verið fleiri einingar sem þú gætir þurft að bæta við ef samþættingin notar umfangsmeiri forritagögn. Eftir að nýja hlutverkið hefur verið búið til er hægt að úthluta því til notanda forritsins.

  - Grunnstarfsmaður (mshr)
  - Umsækjandi til að ráða (mshr)
  - Skírteinishæfni (mshr)
  - Gerð skírteinis (mshr)
  - Fyrirt.  
  - Laun fyrir starfshlutverk (mshr)
  - Laun fyrir tegund starfs (mshr)
  - Land/svæði (mshr)
  - Deild (mshr)
  - Menntunarhæfni (mshr)
  - Prófgráða (mshr)
  - Námsgreinar (mshr)
  - Menntunarkröfur (mshr)
  - Auðkenni (mshr)
  - Gerð auðkennis (mshr)
  - Stofnun (mshr)
  - Útgáfustofnun (mshr)
  - Starfslaun (mshr)
  - Störf (mshr)
  - Menntunarstig (mshr)
  - Tengiliðir aðila (mshr)
  - Fólk (mshr)
  - Aðsetur einstaklinga (mshr)
  - Skoðun einstaklings (mshr)
  - Starfsstaða (mshr)
  - Stöður V2 (mshr)
  - Hæfni starfsreynslu (mshr)
  - Matsstigs (mshr)
  - Matslíkön (mshr)
  - Ástæðukóðar (mshr)
  - Ráðningarbeiðni (mshr)
  - Staðsetning ráðningarbeiðni (mshr)
  - Staða ráðningarbeiðni (mshr)
  - Færni í ráðningarbeiðni (mshr)
  - Skoðunargerð (mshr)
  - Hæfni hæfileika (mshr)
  - Hæfni (mshr)
  - Titlar (mshr)
  - Staða uppgjafahermanns (mshr)
  - Starfsmaður (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Veita forritsheimildir að gögnum Human Resources

Annað skrefið er að tryggja að forritið fái viðeigandi heimildir til að nota gögnin í mannauðsstjórnun með því að tengja þau við notanda í forriti Human Resources. Fyrir notanda forrits eru köll milli þjónusta í gegnum Dataverse sýndartöfllur gerðar í samhengi við auðkenni notandans (forritsins) í Dataverse sem ræsir aðgerðina. Aðlögunarþjónusta sýndartöflunnar flettir þá upp á tengdum notanda í Human Resources og keyrir fyrirspurnina í samhengi við þann notanda. Þetta þýðir að stofna þarf notanda í Human Resources með réttum hlutverkum úthlutað til þess að veita aðgang að gögnum sem samþætt forrit mun nota.

Notandi Human Resources mun einnig þurfa að vera úthlutað réttum heimildum að gögnum í Human Resources. Hlutverkið **Umsókn um ráðningu** (HcmRecruitingIntegrator) er tiltækt með réttindum sem aðalaðilar þurfa til að samþætta við ráðningagögn. Þessu hlutverki er hægt að úthluta til notanda forritsins á síðunni **Notendur** til að veita viðeigandi aðgang að gögnunum. Frekari upplýsingar um öryggishlutverk Human Resources er að finna í [Öryggi byggt á hlutverki](/fin-ops-core/dev-itpro/sysadmin/role-based-security).

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>Setja upp nýjan notanda með viðeigandi heimildum

Til að setja upp nýjan notanda með viðeigandi heimildum skal fylgja þessum skrefum:

  1. Opnaðu síðuna **Notendur** í Human Resources og veldu **Nýr**.
  2. Færðu inn **Notandakenni** og **Notandanafn** fyrir nýjan notanda forritsins. Til dæmis er hægt að slá inn „RecruitingIntegration“.

      > [!NOTE]
      > Ef forritið er ekki með Microsoft Azure Active Directory (Azure AD) notandareikning eða netfang getur þú sett eitthvað eins og „RecruitingApp“ í reitina fyrir netfang og þjónustuaðila fyrir notandann.

  3. Í flýtiflipanum **Hlutverk notanda** velurðu aðgerðina **Úthluta hlutverkum**.
  4. Í glugganum **Úthluta hlutverkum til notanda** skal velja **Umsókn um ráðningu** og velja **Í lagi**.
  5. Vistaðu færslu nýs notanda.

### <a name="link-the-new-human-resources-user-to-the-application"></a>Tengja nýjan notanda Human Resources við forritið

Eftir að notandinn hefur verið stofnaður þarf að búa til færslu fyrir forritið í skjámyndinni **Azure Active Directory Forrit** til að tengja forritið við notanda Human Resources.

  1. Opnaðu skjámyndina **Azure Active Directory Forrit** og veldu **Nýtt**.
  2. Í reitinn **Biðlarakenni** skal færa inn kenni biðlara fyrir notanda forritins sem var búinn til fyrir forritið.
  3. Í reitnum **Heiti** skal færa inn heiti á samþættu forrit.
  4. Í reitnum **Notandakenni** skal velja nýjan notanda Human Resources sem var búinn til fyrir samþættingu ráðningarinnar.
  5. Vistaðu nýju færsluna.

Þá hefur forritið aðgang að gögnum Human Resources sem takmarkast aðeins við gögn sem þarf fyrir samþættingar á umsókn um ráðningu.

## <a name="see-also"></a>Sjá einnig

[Ráða umsækjendur](hr-personnel-recruit.md)<br>
[Hvað er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Nota Microsoft Dataverse vef-API](/powerapps/developer/data-platform/webapi/overview)<br>
[Búa til og uppfæra söfn valkosta með vef-API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
