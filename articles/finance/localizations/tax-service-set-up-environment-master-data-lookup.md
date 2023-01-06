---
title: Virkja uppflettingu aðalgagna fyrir skattaútreikningsstillingar
description: Í þessari grein er útskýrt hvernig á að setja upp og virkja uppflettingu í aðalgögnum skattaútreiknings.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f9d882340171173e5e503f8b5e3aa856e8544b0
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306204"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Virkja uppflettingu aðalgagna fyrir skattaútreikningsstillingar 

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að setja upp og virkja uppflettingu í aðalgögnum skattaútreiknings. Fellilisti er í boði til að velja gildi í grunnstillingu skattaútreiknings fyrir reiti á borð við **Lögaðila**, **Lánardrottnalykil**, **Vörukóða** og **Afhendingarskilmála**. Þessi gildi koma úr tengdu Microsoft Dynamics 365 Finance-umhverfi með því nota Microsoft Dataverse-gagnagjafann.

> [!NOTE] 
> Virkni uppflettingar í aðalgögnum skattaútreiknings er valfrjáls. Hægt er að sleppa eftirfarandi skrefum ef eiginleikinn **Stuðningur við skattþjónustu Dataverse gagnagjafa** í Regulatory Configuration Service (RCS). Fellilistinn er hins vegar í því tilfelli ekki í boði í grunnstillingu skattaútreiknings.

Til að virkja fellilistann í grunnstillingu eiginleikaútgáfu skattaútreiknings skal ljúka eftirfarandi skrefum.

1. [Virkja Microsoft Power Platform-samþættingu og opna Dataverse-umhverfið.](#enable)
2. [Uppsetning fjármála- og rekstrarsýndareininga.](#install)
3. [Skrá forrit Azure Active Directory (Azure AD) forrit.](#register)
4. [Veita forritaheimildir í fjármála- og rekstrarforritum.](#grant)
5. [Skilgreining gagnagjafa sýndareiningar.](#configure)
6. [Virkja Dataverse-sýndareiningar.](#virtual)
7. [Setja upp tengt forrit fyrir skattaútreikning.](#set-up)
8. [Flytja inn og setja upp grunnstillingu Dataverse-líkanavörpunar.](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a>Virkja Microsoft Power Platform-samþættingu og opna Dataverse-umhverfið

Samþætting fjármála- og rekstrarforrita við Microsoft Power Platform er hægt að virkja þegar ný umhverfi fjármála- og rekstrarforrita eru búin til í Microsoft Dynamics Lifecycle Services (LCS). Frekari upplýsingar er að finna í [Microsoft Power Platform samþætting - Yfirlit innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Eftir að þessu er lokið birtist heitið á Microsoft Power Platform-umhverfi í hlutanum **Power Platform Samþætting**.

1. Í LCS, í fjármála- og rekstrarumhverfinu þínu, í hlutanum **Power Platform samþætting** skal finna og skrá hjá sér gildið fyrir **Heiti umhverfis** fyrir tengt umhverfi.

    [![Gildi umhverfisheitis.](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. Í [Power Platform stjórnendamiðstöðinni](https://admin.powerplatform.microsoft.com/environments) í flipanum **Umhverfi** skal velja umhverfið sem passar við gildið **Heiti umhverfis** sem skráð var hjá sér.
3. Á síðunni **Upplýsingar** er að finna gildi **Umhverfisvefslóð** fyrir Dataverse-umhverfið. Taktu niður þetta gildi því þú þarf á því að halda í [Skrefi 7. Setja upp tengt forrit fyrir skattaútreikning](#set-up).
4. Gakktu úr skugga um að þú getir opnað Dataverse umhverfið í vafranum með því velja gildið **Vefslóð umhverfis**.

    [![Dataverse-umhverfissíða.](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > Haltu Dataverse-umhverfinu opnu í vafranum. Þú þarft það í [skrefi 5. Skilgreining gagnagjafa sýndareiningar](#configure).

Frekari upplýsingar er að finna í [Virkja Microsoft Power Platform-samþættinguna](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a>Uppsetning fjármála- og rekstrarsýndareininga

Dataverse lausnin fyrir sýndareiningar fjármála og rekstrar verða að vera uppsettar úr lausn Microsoft AppSource sýndareining.

1. Í AppSource skal finna þess [Sýndareining fjármála- og reksturs](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. Veljið **Fá núna**.
3. Í reitinn **Velja umhverfi** skal færa inn gildið **Heiti umhverfis** sem tekið var niður hér á undan.
4. Veljið gátreitina og svo **Setja upp**.

Að uppsetningu lokinni er hægt að finna forritið **Sýndareining fjármála og reksturs** í [Power Platform stjórnendamiðstöðinni](https://admin.powerplatform.microsoft.com/), undir **Tilföng** \> **Dynamics 365-forrit**.

Frekari upplýsingar er að finna í [Lausn sýndareiningar sótt](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a>Skrá Azure AD-forrit

Þú verður að skrá Azure AD forritið á sama leigjandanum og fjármála- og rekstrarforritin þannig að Dataverse getið kallað á þau.

1. Í [Azure-gáttinni](https://portal.azure.com), skal fara í **Azure Active Directory \> Forritaskráning**.
2. Veljið **Ný skráning** og færið inn eftirfarandi upplýsingar:

    - **Heiti** – Sláðu inn einkvæmt heiti.
    - **Lykilgerð** – Sláið inn **Öll Azure AD-skráasöfn** (einn leigjandi eða margir leigjendur).
    - **Framsenda URI** – Hafa þennan reit auðan.

3. Veldu **Skrá**.
4. Munið gildi **Kenni forrits (biðlari)** því það þarf að nota það síðar.

    [![Azure AD Forrit (biðlari) auðkenningargildi.](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Búa til samhverfulykil fyrir forritið.
6. Veldu **Vottorð og leynd** í nýja forritinu.
7. Veljið **Nýtt leyniorð biðlara**.
8. Sláðu inn lýsingu, veldu gildistíma og veldu svo **Vista**. Lykill verður búinn til og sýndur. Afritið gildið til síðari nota.

Frekari upplýsingar er að finna í [Skráning Azure AD-forrits](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a>Veita forritaheimildir í fjármála- og rekstrarforritum

Dataverse notar Azure AD-forritið sem þú bjóst til til að hringja í forrit fjármála- og reksturs. Því verða fjármála- og rekstrarforrit að geta treyst forritinu og tengja það við notandareikning sem er með viðeigandi réttindi. Í fjármála- og rekstrarforritunum þarf að búa til sérstakan þjónustunotanda sem er **aðeins** með réttindi fyrir virkni sýndareiningarinnar. Þessi notandi þjónustunnar má ekki hafa nein önnur réttindi. Þegar þessu skrefi er lokið geta öll forrit sem eru með leynilykilinn að Azure AD forritinu sem þú bjóst til kallað á umhverfi fjármála- og rekstrarforrita og fengið aðgang að virkni sýndareiningarinnar.

1. Farið í **Kerfisstjórnun** \> **Notendur** \> **Notendur** í umhverfinu.
2. Veldu **Nýr** til að bæta við nýjum notanda og færðu inn eftirfarandi upplýsingar.

    - **Notandakenni** – Sláið inn **dataverseintegration** annað gildi.
    - **Notandanafn** – Sláið inn **dataverseintegration** eða annað gildi.
    - **Veita** – Stillið þennan reit á **NonAAD**.
    - **Tölvupóstur** – Sláið inn **dataverseintegration** annað gildi. (Gildið þarf ekki að vera gilt netfang.)

3. Úthlutið öryggishlutverkinu **forrit samþættingar Dataverse-sýndareiningar** á notandann.
4. Fjarlægja öll önnur hlutverk, þar á meðal **Kerfisnotandi**.
5. Opnið **Kerfisstjórnun** \> **Uppsetning** \> **Azure Active Directory-forrita** til að skrá Dataverse. 
6. Bætið við línu og svo, í reitnum **Biðlarakenni**, skal færa inn **Forritskenni (biðari)** sem skrifað var niður hér á undan.
7. Færið inn lýsandi nafn í reitinn **Heiti**. Til dæmis er slegið inn **Dataverse-samþætting**.
8. Í reitnum **Notandakenni** skal færa inn notandakennið sem var verið að búa til.

Frekari upplýsingar eru í [Veita forritaheimildir í forritum fjármála- og reksturs](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>Skilgreining gagnagjafa sýndareiningar

Þú verður að leggja til Dataverse með forritstilviki fjármála- og reksturs sem á að tengjast.

1. Dataverse umhverfið ætti enn að vera opið í vafranum þínum úr [Skrefi 1. Virkja Microsoft Power Platform samþættingu og opna Dataverse umhverfið](#enable). Veldu stillingarhnappinn (tannhjólið) efst til hægri og veldu svo **Ítarlegar stillingar**.

    [![Opnun ítarlegra stillinga í Dataverse-umhverfinu.](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. Í fellivalmyndinni **Stillingar** skal velja **Stjórnun**.

    [![Stjórnun.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. Veljið **Gagnagjafar sýndareiningar**.

    [![Gagnagjafar sýndareiningar.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. Veldu gagnagjafa sem er nefndur **Finance and Operations**.

    [![Finance and Operations-gagnagjafar.](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Færið inn eftirfarandi upplýsingar úr fyrri skrefum:

    - **Markvefslóð** – Sláið inn vefslóðina þar sem hægt er að opna forrit fjármála- og reksturs.
    - **OAuth-vefslóð** – Sláðu inn `https://login.windows.net/`.
    - **Leigjandakenni** – Tilgreinið leigjanda. Þetta gildi getur verið lénsheiti netfangs fyrirtækisins (til dæmis contoso.com).
    - **Kenni AAD-forrits** – Sláðu inn gildi **Kenni forrits (biðlari)** sem var búið til fyrr.
    - **Leynilykill AAD-forrits** – Sláðu inn leynilykilinn sem var búinn til áður.
    - **AAD-tilfang** – Færið inn **00000015-0000-0000-c000-000000000000**. Þetta gildi er Azure AD-forritið sem táknar Fjármál- og rekstrarforritum. Ætti alltaf að vera þetta sama gildi.

6. Vista breytingarnar.
7. Lokaðu síðunni til að fara aftur á síðuna **Stjórnun** þar sem byrjað verður á [Skrefi 6. Virkja Dataverse sýndareiningar](#virtual).

    [![Lokað fyrir á breytingar á einingunni.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Frekari upplýsingar eru í [Skilgreining gagnagjafa sýndareiningar](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a>Virkja Dataverse-sýndareiningar

Sýnileiki sýndareininga úr fjármála- og rekstrarforritum verður að vera stilltur á **Já** áður en grunnstilling skattaútreiknings getur notað þær.

> [!NOTE]
> Þú getur sleppt þessu skrefi með því að virkja sýndareiningar sem tengjast skattaútreikningi í aðeins einum smelli í [Skrefi 8. Setja upp tengt forrit fyrir skattaútreikning](#import). Hins vegar er mælt með því að virkja að minnsta kosti eina sýndareiningu handvirkt til að gefa til kynna að tengsl milli fjármála- og rekstrarforrita og Dataverse séu komin á.

1. Í Dataverse umhverfinu, á síðunni **Stjórnun**, skal velja síuhnappinn (trektina) efsti til hægri.

    [![Síuhnappur.](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. Í glugganum **Ítarleg leit**, í reitnum **Leita að**, skal velja **Tiltækar einingar Finance and Operations**.
3. Bætið við eftirfarandi reglu: **Heiti** – **Inniheldur** – **CompanyInfoEntity**. Veljið síðan **Niðurstöður**.

    [![Gluggi fyrir ítarlega leit.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Veldu **CompanyInfoEntity** í leitarniðurstöðunum, veldu gátreitinn **Sýnilegt** og veldu síðan **Vista**.

    [![Stilling sýnileika einingar.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Endurtaktu fyrri skref fyrir eftirfarandi einingar sem vísað er til í grunnstillingu skattaútreiknings.

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeading
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Aðeins er hægt að sækja fyrstu 5.000 færslur einingar af Dataverse og þær gerðar aðgengilegar í fellilista í grunnstillingu skattaútreiknings.

Frekari upplýsingar er að finna í [Virkja Microsoft Dataverse sýndareiningar](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a>Setja upp tengt forrit fyrir skattaútreikning

1. Farðu í **Rafræn skýrslugerð** og síðan í hlutanum **Tengdir tenglar** skal velja **Tengd forrit**.

    [![Tengd forrit.](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

2. Veldu **Ný** til að bæta við færslu og færðu inn eftirfarandi upplýsingar.

    - **Heiti** - Sláðu inn nafn.
    - **Gerð** – Veljið **Dataverse**.
    - **Forrit** – Færðu inn Dataverse gildið **Vefslóð umhverfis** fyrir umhverfið sem tekið var niður í [Skrefi 1. Virkja Microsoft Power Platform samþættingu og opna Dataverse umhverfið](#enable).
    - **Leigjandi** – Sláðu inn leigjandann þinn.
    - **Sérsniðin vefslóð** – Sláðu inn Dataverse-vefslóðina og bættu **/api/data/v9.1** við hana.

3. Veldu **Athuga tengingu** og veldu svo í svarglugganum **Smellið hér til að tengjast við valda fjartengt forrit**.

    [![Tenging athuguð.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
4. Ganga þarf úr skugga um „Lokið!“ birtist skilaboð sem gefa til kynna að tengingu hafi verið komið á.

    [![Staðfestingarskilaboð.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)
    
5. Farðu á vinnusvæðið **Eiginleikastjórnun** í RCS og virkjaðu eftirfarandi eiginleika:

    - Altækir eiginleikar
    - Stuðningur við Dataverse gagnagjafa rafrænnar skýrslugerðar
    - Stuðningur við gagnagjafa skattþjónustu Dataverse

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a>Flytja inn og setja upp grunnstillingu Dataverse-líkanavörpunar

Microsoft býður upp á sjálfgefnar grunnstillingar líkanavörpunar fyrir einingar úr fjármála- og rekstrarforritum í skattaútreikning.

1. Í RCS er **Rafræn skýrslugerð** opnað.
2. Í hlutanum **Skilgreiningarveitur** á reitnum **Microsoft** skal velja **Geymslur**.

    [![Geymslur.](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. Veljið færsluna **Altæk skilgreiningargeymsla** og veljið svo **Opna**.
4. Undir **Skattgagnalíka** \> **Gagnalíkan skattaútreiknings** skal velja **Skilgreining gagnalíkans Dataverse**.
5. Í flýtiflipanum **Útgáfur** skal velja útgáfu sem passar við fjármála- og rekstrarforrit og síða velja **Flytja inn**.

    [![Innflutningur skilgreiningar líkanavörpunar í Dataverse.](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > Skilgreining **Dataverse-líkanavörpunar** er aðeins virk á hæstu innfluttu útgáfunni. Því ætti ekki að flytja inn útgáfu af grunnstillingu **Dataverse líkanavörpunar** sem er nýrri en útgáfan af grunnstillingu skattaútreiknings sem ætlunin er að innleiða. Ef þú til dæmis hyggst innleiða útgáfu 40.50.225 af grunnstillingu skattaútreiknings ættirðu aðeins að flytja inn útgáfu 40.50.13 af grunnstillingu **Dataverse líkanavörpunar**. Þú ættir ekki að flytja inn útgáfu 40.54.14. Annars verður misræmi í gagnalíkani í skilgreiningunni.

6. Farið aftur í **Rafræn skýrslugerð** og veljið reitinn **Skilgreiningar skatta**.
7. Veljið innflutta skilgreiningu **Dataverse-líkansvörpunar kortastillingarnar** og svo **Breyta**.
8. Stillið valkostinn **Sjálfgefið fyrir líkanavörpun** á **Já**.
9. Í reitnum **Tengt forrit** skal velja tengda forritið sem var sett upp í [Skrefi 7. Setja upp tengt forrit fyrir skattaútreikning](#set-up).
10. Stilltu valkostinn **Stilla sýnileika sýndartöflu** á **Já** til að stilla allar sýndareiningar sem tengjast skattaútreikningi á að vera sýnilegar.

Þú hefur nú lokið uppsetningu fyrir virkni uppflettingar í aðalgögnum. Fellilisti fyrir reiti eins og **Lögaðila**, **Lánardrottnalykil**, **Vörukóða** og **Afhendingarskilmála** úr Dynamics 365 Finance verður nú virkjaður í uppsetningunni **Útgáfa skattaútreikningsútgáfu**.

[![Lögaðilafellilisti.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
