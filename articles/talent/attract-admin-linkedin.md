---
title: Setja upp samþættingu með LinkedIn fyrir AMicrosoft Dynamics 365 Talent - Attract
description: Þetta efni útskýrir hvernig á að stilla LinkedIn samþættingu fyrir Microsoft Dynamics 365 Talent - Attract svo að þú getir auðveldlega sent inn störf á LinkedIn úr Attract og svo að ráðningaraðilar þínir geti samstillt ráðningarupplýsingar sínar við LinkedIn prófíl umsækjanda.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
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
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6b86cafdf364f2de051f3d8ceab7413c2c13c3a5
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009971"
---
# <a name="set-up-linkedin-integration"></a>Setja upp LinkedIn-samþættingu

[!include[banner](../includes/banner.md)]

Hjálpaðu ráðningaraðilum þínum og ráðningastjórum að laða að hæfileikafólk með því að stilla LinkedIn samþættingu við Microsoft Dynamics 365 Talent: Attract. Attract gerir þér kleift að birta störf beint á LinkedIn, stærsta faglega netkerfinu.

Störf sem þú birtir á LinkedIn í gegnum Attract eru með takmarkaða birtingu og eru veitt fyrirtækinu án aukakostnaðar. Þessar skráningar eru aðeins fáanlegar með hugbúnaðaraðilum LinkedIn, eins og Attract. Þær birtast ekki í glugganum **Starfsferill** á LinkedIn-síðu fyrirtækisins, því aðeins greiddar skráningar birtast þar. Þær er þó sýndar þegar hugsanlegir umsækjendur skoða öll laus störf. Takmarkaðar skráningar eru einnig sýndar í LinkedIn atvinnuleit.

Attract veitir tvær leiðir til að samþætta við LinkedIn til að hjálpa þér að fá umsækjendur frá þessari vinsælu ferilsíðu:

- Birta störf úr Attract á LinkedIn.
- Finna umsækjendur af LinkedIn í Attract.

Þú stillir báða valkostina á flipanum **LinkedIn-samþætting** í stjórnstöðinni. Til að opna stjórnendamiðstöðina ferðu í <https://attract.talent.dynamics.com/adminsettings>.

> [!NOTE]
> Til að nota LinkedIn Recruiter samþættingu við Attract þarftu leyfin [Viðbót við alhliða ráðningar](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) og [LinkedIn Recruiter](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). Sjá frekari upplýsingar, sjá [Hvaða útgáfa af Attract?](./attract-comprehensive-hiring.md).

Ef þú ert í vandræðum með að birta störf á LinkedIn skaltu sjá [Úrræðaleit samþættingar við LinkedIn](./attract-troubleshoot-linkedin.md).

Fyrir upplýsingar um aðrar leiðir til að birta störf á LinkedIn, sjá [Algengar spurningar umLinkedIn](./attract-linkedin-faq.md).

## <a name="configure-job-posting-to-linkedin"></a>Stilla starfsbirtingu á LinkedIn

Áður en þú getur birt störf úr Attract í LinkedIn þarftu [LinkedIn-fyrirtækjakenni](https://aka.ms/findID). Auðkenni fyrirtækis fyrir LinkedIn er númeraröð sem staðfestir á einkvæman hátt fyrirtækið þitt á LinkedIn. Fyrir frekari upplýsingar um kenni fyrirtækisins á LinkedIn, sjá [Að tengja fyrirtækjakenni við atvinnutorgið á LinkedIn - algengar spurningar](https://aka.ms/findID).

Attract sendir streymi af starfsbirtingum þínum til LinkedIn og LinkedIn athugar hvort streymið sé um það bil einu sinni á dag. Það getur tekið allt að 48 klukkustundir fyrir störf þín að birtast á svæðinu.

Störf sem eru auglýst á LinkedIn birtast á LinkedIn-svæðinu. LinkedIn er ekki með prófunarumhverfi til að birta störf. Þess vegna skaltu ganga úr skugga um að þú birtir engin prófunarstörf óvart. 

1. Í **Uppsetning** valmyndinni (táknið fyrir gír) efst í hægra horninu skaltu velja **Stjórnstöð**. Að öðrum kosti geturðu farið á <https://attract.talent.dynamics.com/adminsettings>.
2. Veldu flipann **Samþætting við LinkedIn**.
3. Undir **Heiti fyrirtækis** slærðu inn heiti fyrirtækisins og undir **Kenni fyrirtækis** slærðu inn fyrirtækjakenni þitt á LinkedIn. Gakktu úr skugga um að heiti fyrirtækisins passi við heitið sem birtist á LinkedIn síðu fyrirtækisins. Fyrir frekari upplýsingar um kenni fyrirtækisins á LinkedIn, sjá [Að tengja fyrirtækjakenni við atvinnutorgið á LinkedIn - algengar spurningar](https://www.linkedin.com/help/linkedin/answer/98972).

    Ef þú þarft að breyta upplýsingum fyrir fyrirtækið skaltu sjá [Breyta heimilisfangi fyrirtækisins, tæknilegum tengiliðum og fleira](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). Ef vandamál eru enn til staðar skaltu hafa samband við [Notandaþjónusta LinkedIn](https://www.linkedin.com/help/linkedin).

4. Veljið **Vista**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Setja upp LinkedIn Recruiter með Attract 

Til að leyfa ráðningaraðilum að finna störf í gegnum LinkedIn Recruiter verður þú að stilla samþættingu við LinkedIn Recruiter í Attract. Til að ljúka skilgreiningarferlinu verður þú að vinna með notandanum sem er stjórnandi á LinkedIn Recruiter samningi fyrirtækisins.

1. Í **Uppsetning** valmyndinni (táknið fyrir gír) efst í hægra horninu skaltu velja **Stjórnstöð**. Að öðrum kosti geturðu farið á <https://attract.talent.dynamics.com/adminsettings>.
2. Veldu flipann **Samþætting við LinkedIn**.

    [![Yfirlit Attract stjórnanda til að hefja LinkedIn Recruiter-samþættingu](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Veldu **Tengjast** til að hefja uppsetninguna. Þér verður leiðbeint í gegnum innskráningarferlið í LinkedIn.
4. Ef þú hefur sæti á mörgum LinkedIn samningum skaltu velja samninginn sem þú vilt tengja við Attract-kerfið. Ef þú hefur aðeins pláss á einum LinkedIn-samningi geturðu sleppt þessu skrefi.
5. Fyrir neðan **Recruiter System Connect (RSC)** smellirðu á **Beiðni**.

    [![Yfirlit Attract stjórnanda til að biðja um LinkedIn Recruiter-samþættingu](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. Núna ætti stillingin **Recruiter System Connect (RSC)** að birtast sem **Samstarfsaðili tilbúinn**. Ef þú sérð **Tilkynna samstarfsaðila** á þessari síðu skaltu bíða í nokkrar sekúndur, velja **Tilkynna samstarfsaðila** og endurnýja síðan síðuna. Nú ætti stillingin að birtast sem **Samstarfsaðili tilbúinn**.

    [![Yfirlit Attract-sjórnanda til að gefa til kynna beiðnum Attract megin hefur verið lokið](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. Til að ljúka eftirfarandi skrefum þarftu að hafa stjórnandaréttindi á LinkedIn Recruiter samningnum.

    1. Skráðu þig inn á LinkedIn með því að nota stjórnandareikninginn þinn og veldu síðan **LinkedIn Recruiter** efst til hægri. 
    2. Í valmyndinni **Fleira** efst á síðunni velurðu á **stjórnandastillingar** og veldu síðan flipann **ATS**.
    3. Til að virkja útflutning með einum smelli fyrir aðeins einn samning kveikirðu á **Aðgangur að samningi (fyrir hvert sæti í þessum samningi**. Til að virkja hann fyrir allt fyrirtækið kveikirðu á **Aðgangstig fyrirtækis (fyrir hvern samning í fyrirtækinu þínu**.

    [![Kveikja á Attract-samþættingu úr LinkedIn Recruiter yfirliti stjórnanda](./media/EnableRSC.png)](./media/EnableRSC.png)

8. Í stjórnstöð Attract velurðu flipann **LinkedIn-samþætting**. Nú ætti stillingin **Recruiter System Connect (RSC)** að birtast sem **Virk**.

    [![LinkedIn Recruiter samþættingu lokið](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>Setja upp Sækja um með LinkedIn í Attract

Þú getur leyft umsækjendum að sækja um störf þín með LinkedIn-forstillingum sínum. Fyrir frekari upplýsingar um Sækja um með LinkedIn, sjá [Máttur LinkedIn alls staðar: Sæktu um með LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

Þessi eiginleiki er í forútgáfu sem stendur. Áður en þú fylgir þessum skrefum skaltu ganga úr skugga um að Sækja um með LinkedIn sé virkt. Nánari upplýsingar um virkjun á forskoðunareiginleikum er að finna í [Fá aðgang að forskoðunareiginleikum í Talent](./access-preview-feature.md).

1. Í **Uppsetning** valmyndinni (táknið fyrir gír) efst í hægra horninu skaltu velja **Stjórnstöð**. Að öðrum kosti geturðu farið á <https://attract.talent.dynamics.com/adminsettings>.
2. Veldu flipann **Samþætting við LinkedIn**.

    [![Yfirlit Attract stjórnanda til að hefja LinkedIn Recruiter-samþættingu](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Við hliðina á **Sækja um með LinkedIn** velurðu **Tengjast** til að hefja uppsetninguna. Þér verður leiðbeint í gegnum afganginn af ferlinu í LinkedIn.

## <a name="see-also"></a>Sjá einnig

[Algengar spurningar um LinkedIn](./attract-linkedin-faq.md)

[Birta störf á utanaðkomandi svæðum úr Attract](./posting-jobs-external.md)

[Finna umsækjendur með LinkedIn Recruiter](./attract-linkedin-recruiter.md)

[Stofna störf](./creating-jobs-attract.md)

[Úrræðalaeit samþættingar við LinkedIn](./attract-troubleshoot-linkedin.md)
