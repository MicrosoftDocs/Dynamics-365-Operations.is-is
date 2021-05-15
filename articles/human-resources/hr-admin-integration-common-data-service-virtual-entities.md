---
title: Skilgreina Dataverse-sýndartöflur
description: Þetta efnisatriði sýnir hvernig á að skilgreina sýndartöflur fyrir Dynamics 365 Human Resources. Búið til og uppfærið fyrirliggjandi sýndartöflur og greinið tiltækar töflur sem hafa verið búnar til.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 04997aba427ae6013c8154593b09ae1a45a580c3
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935754"
---
# <a name="configure-dataverse-virtual-tables"></a>Skilgreina Dataverse-sýndartöflur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources er sýndargagnagjafi í Microsoft Dataverse. Hann býður upp á heildstæðar aðgerðir stofnunar, lesturs, uppfærslu og eyðingar (CRUD) úr Dataverse og Microsoft Power Platform. Gögn fyrir sýndartöflur eru ekki geymd í Dataverse, heldur í gagnagrunni forritsins.

Til að virkja CRUD-aðgerðir í einingum Human Resources úr Dataverse þarf að bjóða upp á einingarnar sem sýndartöflur í Dataverse. Þetta gerir þér kleift að framkvæma CRUD-aðgerðir í Dataverse og Microsoft Power Platform á gögnum sem eru í Human Resources. Aðgerðirnar styðja einnig sannprófanir á viðskiptagrunni Human Resources til að tryggja heilleika gagna þegar gögn eru skrifuð í einingarnar.

> [!NOTE]
> Mannauðseiningar samsvara Dataverse töflum. Frekari upplýsingar um Dataverse (áður Common Data Service) og uppfærslur á hugtökum er að finna í [Hvað er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Tiltækar sýndartöflur fyrir Human Resources

Allar einingar Open Data Protocol (OData) í Human Resources eru í boði sem sýndartöflur í Dataverse. Þetta er einnig tiltækt í Power Platform. Nú er hægt að búa til forrit og upplifanir með gögnum beint úr Human Resources með fullum CRUD-möguleikum án þess að afrita eða samstilla gögn við Dataverse. Hægt er að nota Power Apps-gáttir til að smíða útlit vefsvæða sem bjóða upp á samvinnu fyrir viðskiptaferla í Human Resources.

Hægt er að skoða lista yfir sýndartöflur sem eru virkjaðar í umhverfinu og byrja að vinna með töflurnar í [Power Apps](https://make.powerapps.com) í lausninni **Sýndartöflur HR í Dynamics 365**.

![Sýndartöflur HR í Dynamics 365 í Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>Sýndartöflur í samanburði við venjulegar töflur

Sýndartöflur fyrir Human Resources eru ekki þær sömu og venjulegu Dataverse-töflurnar sem búnar eru til fyrir Human Resources. 

Venjulegu töflurnar fyrir Human Resources eru myndaðar sérstaklega og unnið með þær í lausn HCM Common í Dataverse. Með venjulegum töflum eru gögnin geymd í Dataverse og þarfnast samstillingar við gagnagrunn Human Resources-forritsins.

> [!NOTE]
> Til að sjá lista yfir venjulegar Dataverse-töflur fyrir Human Resources skal fara í [Dataverse-töflur](./hr-developer-entities.md).

## <a name="setup"></a>Setja upp

Fylgið þessum uppsetningarskrefum til að virkja sýndartöflur í umhverfinu.

### <a name="enable-virtual-tables-in-human-resources"></a>Virkja sýndartöflur í Human Resources

Fyrst þarf að virkja sýndartöflur í vinnusvæðinu **Eiginleikastjórnun**.

1. Veldu í Human Resources **Kerfisstjórnun**.

2. Veldu reitinn **Stjórnun eiginleika**.

3. Veldu **Stuðningur sýndartöflu fyrir HR í Dataverse** og veldu því næst **Virkja**.

Frekari upplýsingar um virkjun og óvirkjun eiginleika er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Skrá forritið í Microsoft Azure

Skrá þarf Human Resources tilvikið inn í Azure-gáttinni þannig að auðkenningarverkvangur Microsoft geti veitt sannvottunar- og leyfisþjónustu fyrir forritið og notendur. Frekari upplýsingar um skráningu forrita í Azure er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app).

1. Opnið [Microsoft Azure-gáttina](https://portal.azure.com)

2. Í listanum yfir Azure-þjónustur skal velja **Skráning forrita**.

3. Veljið **Ný skráning**.

4. Í reitinn **Heiti** skal færa inn lýsandi heiti á forritinu. Til dæmis **Dynamics 365 Human Resources Sýndartöflur**.

5. Í reitinn **Framsenda API** skal færa inn nafnarými vefslóðar fyrir tilvikið af Human Resources.

6. Veldu **Skrá**.

7. Þegar skráningu lýkur birtir Azure-gáttin svæðið **Yfirlit** fyrir skráningu forritsins, sem felur í sér **Forritskenni (biðlari)**. Takið niður **Forritskennið (biðlari)** á þessari stundu. Þessar upplýsingar verða færðar inn þegar á að [Skilgreina gagnagjafa sýndartöflu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

8. Á vinstra yfirlitssvæðinu skal velja **Vottorð og leynilyklar**.

9. Í hlutanum **Leynilyklar biðlara** á síðunni skal velja **Nýrr leynilykill biðlara**.

10. Gefið upp lýsingu, veljið tímalengd og veljið **Bæta við**.

11. Skráðu gildi leyndarmálsins úr **Gildi** eiginleika töflunnar. Þessar upplýsingar verða færðar inn þegar á að [Skilgreina gagnagjafa sýndartöflu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

    > [!IMPORTANT]
    > Gætið þess að taka niður gildi leynilykilsins að svo stöddu. Leynilykillinn er ekki sýndur aftur eftir að farið er af þessari síðu.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>Setja upp forritið Dynamics 365 Virtual Table

Setja skal upp forritið Dynamics 365 HR Virtual Table í Power Apps-umhverfinu til að virkja lausnapakka sýndartöflunnar í Dataverse.

1. Í Human Resources skal opna síðuna **Microsoft Dataverse-samþætting**.

2. Veljið flipann **Sýndartöflur**.

3. Veljið **Setja upp sýndartöfluforrit**.

### <a name="configure-the-virtual-table-data-source"></a>Skilgreina gagnagjafa sýndartöflu

Næsta skref er að skilgreina gagnagjafa sýndartöflu í Power Apps-umhverfinu.

1. Opna [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).

2. Í listanum **Umhverfi** er valið Power Apps-umhverfi sem tengist tilviki Human Resources.

3. Veljið **Vefslóð umhverfis** í hlutanum **Upplýsingar** á síðunni.

4. Í **heilsulausnarmiðstöð** skal velja táknið **Ítarleg leit** efst til hægri á forritssíðunni.

5. Á síðunni **Ítarleg leit**, í fellilistanum **Leita að**, skal velja **Finance and Operations Grunnstillingar sýndargagnagjafa**.

   > [!NOTE]
   > Uppsetning sýndartöfluforritsins úr fyrra uppsetningarskrefi getur tekið nokkrar mínútur. Ef **Finance and Operations Skilgreiningar sýndargagnagjafa** eru ekki í boði í listanum skal hinkra smástund og svo uppfæra listann.

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
- Forritið Dynamics 365 HR Virtual Table sem var sett upp í Power Apps-umhverfinu 

1. Í Human Resources skal opna síðuna **Azure Active Directory-forrit**.

2. Velja skal **Ný** til að búa til nýja færslu forrits:

    - Í reitinn **Biðlarakenni** skal færa inn kenni biðlara fyrir forritið sem var skráð í Microsoft Azure-gáttina.
    - Í reitinn **Heiti** skal færa inn heiti forritsins sem var skráð í Microsoft Azure-gáttina.
    - Í reitinn **Notandakenni** skal velja notandakenni notanda með stjórnandaheimildir í Human Resources og Power Apps-umhverfinu.

3. Veljið **Ný** til að búa til aðra færslu forrits:

    - **Auðkenni biðlara**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Heiti**: Dynamics 365 HR Virtual Table
    - Í reitinn **Notandakenni** skal velja notandakenni notanda með stjórnandaheimildir í Human Resources og Power Apps-umhverfinu.

## <a name="generate-virtual-tables"></a>Mynda sýndartöflur

Þegar uppsetningu er lokið er hægt að velja sýndartöflurnar sem á að mynda og virkja í Dataverse-tilvikinu.

1. Í Human Resources skal opna síðuna **Microsoft Dataverse-samþætting**.

2. Veljið flipann **Sýndartöflur**.

> [!NOTE]
> **Virkjar sýndartöflur** verður stillt á **Já** sjálfkrafa þegar allri nauðsynlegri uppsetningu er lokið. Ef skipting er stillt á **Nei** skal fara yfir skrefin í fyrri hlutum þessa skjals til að tryggja að uppsetningu forútgáfu sé lokið.

3. Veljið töfluna eða töflurnar sem á að búa til í Dataverse.

4. Velja **Búa til/uppfæra**.

![Dataverse Samþætting](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>Athuga myndunarstöðu töflu

Sýndartöflur eru myndaðar í Dataverse í gegnum ósamstillta bakgrunnsvinnslu. Uppfærslur á ferlinu birtast í aðgerðamiðstöð. Upplýsingar um ferlið, þar á meðal villukladda, birtast á síðunni **Sjálfvirkni ferlis**.

1. Í Human Resources skal opna síðuna **Sjálfvirkni ferlis**.

2. Veljið flipann **Bakgrunnsvinnslur**.

3. Veljið **Bakgrunnsvinnsla á ósamstilltri aðgerð sýndartöflukönnunar**.

4. Veldu **Skoða síðustu niðurstöður**.

Hlðarsvæði sýnir nýjustu niðurstöður framkvæmdarinnar fyrir ferlið. Hægt er að skoða kladda vinnslunnar, þar á meðal allar villur sem skilað er frá Dataverse.

## <a name="see-also"></a>Sjá einnig

[Hvað er Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Töflur í Dataverse](/powerapps/maker/common-data-service/entity-overview)<br>
[Yfirlit töflutengsla](/powerapps/maker/common-data-service/relationships-overview)<br>
[Stofna og breyta sýndartöflum sem innihalda gögn frá ytri gagnagjafa](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Hvað eru Power Apps-gáttir?](/powerapps/maker/portals/overview)<br>
[Yfirlit yfir stofnun forrita í Power Apps](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
