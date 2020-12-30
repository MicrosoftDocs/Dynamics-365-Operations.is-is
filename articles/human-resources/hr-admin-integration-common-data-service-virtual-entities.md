---
title: Skilgreina sýndareiningar Common Data Service
description: Þetta efnisatriði sýnir hvernig á að skilgreina sýndareiningar fyrir Dynamics 365 Human Resources. Búið til og uppfærið fyrirliggjandi sýndareiningar og greinið tiltækar einingar sem hafa verið búnar til.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645602"
---
# <a name="configure-common-data-service-virtual-entities"></a>Skilgreina sýndareiningar Common Data Service

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources er sýndargagnagjafi í Common Data Service. Hann býður upp á heildstæðar aðgerðir stofnunar, lesturs, uppfærslu og eyðingar (CRUD) úr Common Data Service og Microsoft Power Platform. Gögn fyrir sýndareiningar eru ekki geymd í Common Data Service, heldur í gagnagrunni forritsins. 

Til að virkja CRUD-aðgerðir í Common Data Service, þarf að bjóða upp á einingarnar sem sýndareiningar í Common Data Service. Þetta gerir þér kleift að framkvæma CRUD-aðgerðir í Common Data Service og Microsoft Power Platform á gögnum sem eru í Human Resources. Aðgerðirnar styðja einnig sannprófanir á viðskiptagrunni Human Resources til að tryggja heilleika gagna þegar gögn eru skrifuð í einingarnar.

## <a name="available-virtual-entities-for-human-resources"></a>Tiltækar sýndareiningar fyrir Human Resources

Allar einingar Open Data Protocol í Human Resources eru í boði sem sýndareiningar í Common Data Service. Þetta er einnig tiltækt í Power Platform. Nú er hægt að búa til forrit og upplifanir með gögnum beint úr Human Resources með fullum CRUD-möguleikum án þess að afrita eða samstilla gögn við Common Data Service. Hægt er að nota Power Apps-gáttir til að smíða útlit vefsvæða sem bjóða upp á samvinnu fyrir viðskiptaferla í Human Resources.

Hægt er að skoða lista yfir sýndareiningar sem eru virkjaðar í umhverfinu og byrja að vinna með einingarnar í [Power Apps](https://make.powerapps.com) í lausninni **Sýndareiningar HR í Dynamics 365**.

![Sýndareiningar HR í Dynamics 365 í Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Sýndareiningar í samanburði við venjulegar einingar

Sýndareiningar fyrir Human Resources eru ekki þær sömu og venjulegu Common Data Service-einingarnar sem búnar eru til fyrir Human Resources. Venjulegu einingarnar fyrir Human Resources eru myndaðar sérstaklega og unnið með þær í HCM Common Solution í Common Data Service. Með venjulegum einingum eru gögnin geymd í Common Data Service og þarfnast samstillingar við gagnagrunn Human Resources-forritsins.

> [!NOTE]
> Til að sjá lista yfir venjulegar Common Data Service-einingar fyrir Human Resources skal fara í [Common Data Service einingar](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>Setja upp

Fylgið þessum uppsetningarskrefum til að virkja sýndareiningar í umhverfinu.

### <a name="enable-virtual-entities-in-human-resources"></a>Virkja sýndareiningar fyrir Human Resources

Fyrst þarf að virkja sýndareiningar í vinnusvæðinu **Eiginleikastjórnun**.

1. Veldu í Human Resources **Kerfisstjórnun**.

2. Veldu reitinn **Stjórnun eiginleika**.

3. Veljið **Stuðningur við sýndareiningu í HR/CDS** og svo **Virkja**.

Frekari upplýsingar um virkjun og óvirkjun eiginleika er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Skrá forritið í Microsoft Azure

Skrá þarf Human Resources tilvikið inn í Azure-gáttinni þannig að auðkenningarverkvangur Microsoft geti veitt sannvottunar- og leyfisþjónustu fyrir forritið og notendur. Frekari upplýsingar um skráningu forrita í Azure er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Opnið [Microsoft Azure-gáttina](https://portal.azure.com)

2. Í listanum yfir Azure-þjónustur skal velja **Skráning forrita**.

3. Veljið **Ný skráning**.

4. Í reitinn **Heiti** skal færa inn lýsandi heiti á forritinu. Til dæmis, **Dynamics 365 Human Resources Sýndareiningar**.

5. Í reitinn **Framsenda API** skal færa inn nafnarými vefslóðar fyrir tilvikið af Human Resources.

6. Veldu **Skrá**.

7. Þegar skráningu lýkur birtir Azure-gáttin svæðið **Yfirlit** fyrir skráningu forritsins, sem felur í sér **Forritskenni (biðlari)**. Takið niður **Forritskennið (biðlari)** á þessari stundu. Þessar upplýsingar verða færðar inn þegar á að [Skilgreina gagnagjafa sýndareiningar](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. Á vinstra yfirlitssvæðinu skal velja **Vottorð og leynilyklar**.

9. Í hlutanum **Leynilyklar biðlara** á síðunni skal velja **Nýrr leynilykill biðlara**.

10. Gefið upp lýsingu, veljið tímalengd og veljið **Bæta við**.

11. Skráið gildi fyrir leynilykil. Þessar upplýsingar verða færðar inn þegar á að [Skilgreina gagnagjafa sýndareiningar](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > Gætið þess að taka niður gildi leynilykilsins að svo stöddu. Leynilykillinn er ekki sýndur aftur eftir að farið er af þessari síðu.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Setja upp forritið Dynamics 365 HR Virtual Entity

Setja skal upp forritið Dynamics 365 HR Virtual Entity í Power Apps-umhverfinu til að virkja lausnapakka sýndareiningarinnar í Common Data Service.

1. Opna [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).

2. Í listanum **Umhverfi** er valið Power Apps-umhverfi sem tengist tilviki Human Resources.

3. Í hlutanum **Tilföng** á síðunni skal velja **Dynamics 365-forrit**.

4. Veljið aðgerðina **Setja upp forrit**.

5. Veljið **Dynamics 365 HR Virtual Entity** og veljið **Áfram**.

6. Yfirfara og merkja til að samþykkja þjónustuskilmála.

7. Velja **Setja upp**.

Uppsetningin tekur örfáar mínútur. Þegar henni lýkur skal halda áfram í næsta skref.

![Setja upp forritið Dynamics 365 HR Virtual Entity úr Power Platform-stjórnendamiðstöðinni](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>Skilgreining gagnagjafa sýndareiningar 

Næsta skref er að skilgreina gagnagjafa sýndareiningar í Power Apps-umhverfinu. 

1. Opna [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).

2. Í listanum **Umhverfi** er valið Power Apps-umhverfi sem tengist tilviki Human Resources.

3. Veljið **Vefslóð umhverfis** í hlutanum **Upplýsingar** á síðunni.

4. Í **heilsulausnarmiðstöð** skal velja táknið **Ítarleg leit** efst til hægri á forritssíðunni.

5. Á síðunni **Ítarleg leit**, í fellilistanum **Leita að**, skal velja **Finance and Operations Grunnstillingar sýndargagnagjafa**.

6. Veldu **Niðurstöður**.

7. Veljið færsluna **Microsoft HR-gagnagjafi**.

8. Færa skal inn nauðsynlegar upplýsingar fyrir skilgreiningu gagnagjafans:

   - **Markvefslóð**: Vefslóð nafnarýmis Human Resources. Snið URL viðtöku er:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     Dæmi:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Gætið þess að taka „**/**“ stafinn með í lok vefslóðarinnar til að forðast villu.

   - **Auðkenni leigjanda**: Azure Active Directory (Azure AD) leigjandakenni.

   - **AAD-forritskenni**: Forritskennið (biðlarinn) sem er stofnað fyrir forritið sem er skráð í Microsoft Azure-gáttina. Þú fékkst þessar upplýsingar fyrr í skrefinu [Skrá forritið í Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **Leynilykill AAD-forrits**: Leynilykill biðlara sem er stofnað fyrir forritið sem er skráð í Microsoft Azure-gáttina. Þú fékkst þessar upplýsingar fyrr í skrefinu [Skrá forritið í Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![Microsoft HR-gagnagjafi](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Veljið **Vista og loka**.

### <a name="grant-app-permissions-in-human-resources"></a>Veita forritsheimildir í Human Resources

Veitið heimildir fyrir tvö Azure AD-forrit í Human Resources:

- Forritið sem var stofnað fyrir leigjanda í Microsoft Azure gáttinni
- Forritið Dynamics 365 HR Virtual Entity sem var sett upp í Power Apps-umhverfinu 

1. Í Human Resources skal opna síðuna **Azure Active Directory-forrit**.

2. Velja skal **Ný** til að búa til nýja færslu forrits:

    - Í reitinn **Biðlarakenni** skal færa inn kenni biðlara fyrir forritið sem var skráð í Microsoft Azure-gáttina.
    - Í reitinn **Heiti** skal færa inn heiti forritsins sem var skráð í Microsoft Azure-gáttina.
    - Í reitinn **Notandakenni** skal velja notandakenni notanda með stjórnandaheimildir í Human Resources og Power Apps-umhverfinu.

3. Veljið **Ný** til að búa til aðra færslu forrits:

    - **Auðkenni biðlara**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Heiti**: Dynamics 365 HR Virtual Entity
    - Í reitinn **Notandakenni** skal velja notandakenni notanda með stjórnandaheimildir í Human Resources og Power Apps-umhverfinu.

## <a name="generate-virtual-entities"></a>Mynda sýndareiningar

Þegar uppsetningu er lokið er hægt að velja sýndareiningarnar sem á að mynda og virkja í Common Data Service-tilvikinu.

1. Í Human Resources skal opna síðuna **Common Data Service (CDS)-samþætting**.

2. Veldu flipann **Sýndareiningar**.

> [!NOTE]
> **Virkjar sýndareininguna** verður stillt á **Já** sjálfkrafa þegar allri nauðsynlegri uppsetningu er lokið. Ef skipting er stillt á **Nei** skal fara yfir skrefin í fyrri hlutum þessa skjals til að tryggja að uppsetningu forútgáfu sé lokið.

3. Velja skal eininguna eða einingarnar sem á að búa til í Common Data Service.

4. Velja **Búa til/uppfæra**.

![Common Data Service Samþætting](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a>Athuga einingu um myndunarstöðu

Sýndareiningar eru myndaðar í Common Data Service í gegnum ósamstillta bakgrunnsvinnslu. Uppfærslur á ferlinu birtast í aðgerðamiðstöð. Upplýsingar um ferlið, þar á meðal villukladda, birtast á síðunni **Sjálfvirkni ferlis**.

1. Í Human Resources skal opna síðuna **Sjálfvirkni ferlis**.

2. Veljið flipann **Bakgrunnsvinnslur**.

3. Velið **Virtual einingakönnun async Aðgerðar bakgrunnsvinnsla**.

4. Veldu **Skoða síðustu niðurstöður**.

Hlðarsvæði sýnir nýjustu niðurstöður framkvæmdarinnar fyrir ferlið. Hægt er að skoða kladda vinnslunnar, þar á meðal allar villur sem skilað er frá Common Data Service.

## <a name="see-also"></a>Sjá einnig

[Hvað er Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Einingayfirlit](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Yfirlit einingartengsla](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Stofna og breyta sýndareiningum sem innihalda gögn frá ytri gagnagjafa](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Hvað eru Power Apps-gáttir?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Yfirlit yfir stofnun forrita í Power Apps](https://docs.microsoft.com/powerapps/maker/)
