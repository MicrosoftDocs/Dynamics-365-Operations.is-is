---
title: Uppfæra í altæka aðila- og aðsetursbókarlíkanið
description: Í þessu efnisatriði er lýst hvernig á að uppfæra gögn tvöfaldrar skráningar í aðilalíkanið og líkan altækrar aðsetursbókar.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857371"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Uppfæra í altæka aðila- og aðsetursbókarlíkanið

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Sniðmát Azure Data Factory](https://aka.ms/dual-write-gab-adf) hjálpar til við að uppfæra fyrirliggjandi töflugögn **Lykils**, **Tengiliðar** og **Lánardrottins** í tvöfaldri skráningu í aðilalíkanið og líkan altækrar aðsetursbókar. Sniðmátið afstemmir gögnin úr bæði Finance and Operations-forritum og forritum viðskiptavinar. Undir lok ferlisins verða reitirnir **Aðili** og **Tengiliður** fyrir **Aðilafærslur** búnir til og tengdir við færslur **Lykils**, **Tengiliðar** og **Lánardrottins** í forritum viðskiptavinar. .csv skrá (`FONewParty.csv`) er mynduð til að stofna nýjar **Aðilafærslur** í Finance and Operations-forritinu. Í þessu efnisatriði er að finna leiðbeiningar um notkun Data Factory-sniðmáts og uppfærslu gagnanna.

Ef engar sérstillingar eru til staðar er hægt að nota sniðmátið eins og það er. Ef sérstillingar eru fyrir hendi fyrir **Lykil**, **Tengilið** og **Lánardrottin** þarf að breyta sniðmátinu samkvæmt eftirfarandi leiðbeiningum.

> [!Note]
> Sniðmátið hjálpar til við að uppfæra eingöngu gögn **Aðila**. Í síðari útgáfu verða póstföng og rafræn heimilisföng höfð með.

## <a name="prerequisites"></a>Forkröfur

Þessar forkröfur eru nauðsynlegar:

+ [Azure-áskrift](https://portal.azure.com/)
+ [Aðgangur að sniðmáti](https://aka.ms/dual-write-gab-adf)
+ Þú ert núverandi viðskiptavinur tvöföldrar skráningar.

## <a name="prepare-for-the-upgrade"></a>Uppfærsla undirbúin

+ **Full samstilling**: Bæði umhverfinu eru samstillt að fullu fyrir **Lykil (viðskiptavinur)**, **Tengilið** og **Lánardrottin**.
+ **Samþættingarlyklar**: Töflur **Lykils (viðskiptavinur)**, **Tengiliðar** og **Lánardrottins** í forritum viðskiptavinar nota tilbúna samþættingarlykla sem fylgja með. Ef samþættingarlyklarnir voru sérstilltir þarf að sérstilla sniðmátið.
+ **Aðilanúmer**: Allar færslur **Lykils (viðskiptavinar)**, **Tengiliðar** og **Lánardrottins** sem verða uppfærðar eru með númer **Aðila**. Færslur án númers **Aðila** verða hunsaðar. Ef uppfæra á þær færslur skal bæta númeri **Aðila** við þær áður en uppfærsluferlið er sett í gang.
+ **Stöðvun kerfis**: Í uppfærsluferlinu þarf að slökkva á nettengingu fyrir bæði umhverfi Finance and Operations og umhverfi viðskiptavinar.
+ **Skyndimynd**: Takið skyndimyndir af bæði forritum Finance and Operations og viðskiptavinar. Notið skyndimyndirnar til að endurheimta fyrri stöðu ef á þarf að halda.

## <a name="deployment"></a>Nýting

1. Sækið sniðmátið úr [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).

2. Skráðu þig inn á [Microsoft Azure](https://portal.azure.com/).

3. Stofnið [tilfangaflokk](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).

4. Búið til [geymslureikning](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) í tilfangaflokknum sem var stofnaður.

5. Stofnið [gagnasmiðju](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) í ofangreindum tilfangaflokki sem var stofnaður.

6. Opnið gagnasmiðjuna og veljið reitinn **Stýra og fylgjast með**.

7. Í flipanum **Stjórna** skal velja **ARM-sniðmát**.

8. Veljið **Flytja inn ARM-sniðmát** til að flytja inn sniðmátið **Aðili**.

9. Flytjið sniðmátið inn í gagnasmiðjuna. Færið inn eftirfarandi gildi fyrir **Upplýsingar um verk** og **Upplýsingar um tilvik**.

    Svæði | Virði
    ---|---
    Áskrift | Azure-áskrift
    Tilfangaflokkur | Gefið upp sama tilfang þar sem geymslureikningur er stofnaður fyrir.
    Svæði | Tilgreina svæði.
    Heiti verksmiðju | Tilgreina heiti verksmiðju.
    FO Linked Service_service Principal Key | Tilgreinið forritslykilinn.
    Strengur Azure Blob Storage_connection | Tengingarstrengur Azure Blob Storage.
    Dynamics Crm Linked Service_password | Aðgangsorðið fyrir notandareikninginn sem tilgreindur var sem notandanafnið.
    FO Linked Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO Linked Service_properties_type Properties_tenant | Tilgreinið upplýsingar um leigjanda (heiti léns eða leigjandakenni) sem forritið heyrir undir.
    FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO Linked Service_properties_type Properties_service Principal Id | Tilgreinið biðlarakenni forritsins.
    Dynamics Crm Linked Service_properties_type Properties_username | Notandanafnið sem á að tengja Dynamics.

    Frekari upplýsingar er að finna í [Úthluta sniðmáti forðastjóra handvirkt fyrir hvert umhverfi](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Tengdir þjónustueiginleikar](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties) og [Afrita gögn með Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Eftir uppsetningu skal staðfesta gagnasöfnin, gagnaflæðið og tengda þjónustu gagnasmiðjunnar.

   ![Gagnasafn, gagnaflæði og tengd þjónusta](media/data-factory-validate.png)

11. Farið í **Stjórna**. Undir **Tengingar** skal velja **Tengd þjónusta**. Veljið **DynamicsCrmLinkedService**. Á skjámyndinni **Breyta tengdri þjónustu (Dynamics CRM)** skal færa inn eftirfarandi gildi:

    Svæði | Virði
    ---|---
    Nafn | DynamicsCrmLinkedService
    lýsing | Tengdar þjónustur til að tengjast við CRM-tilvik til að sækja gögn eininga
    Tengjast með keyrslutíma samþættingar | AutoResolvelntegrationRuntime
    Uppsetningargerð | Nettenging
    Uri þjónustu | `https://<organization-name>.crm[x].dynamics.com`
    Sannvottunargerð | Office365
    Notandanafn |
    Aðgangsorð eða Azure-lyklageymsla | Aðgangsorð
    Aðgangsorð |

## <a name="run-the-template"></a>Keyra sniðmátið

1. Stöðvið eftirfarandi tvöfalda skráningu **Lykils**, **Tengiliðar** og **Lánardrottins** með Finance and Operations-forritinu.

    + Viðskiptavinir V3 (lyklar)
    + Viðskiptavinir V3 (tengiliðir)
    + CDS Tengiliðir V2 (tengiliðir)
    + CDS Tengiliðir V2 (tengiliðir)
    + Lánardrottinn V2 (msdyn_vendors)

2. Gangið úr skugga um að varpanir séu fjarlægðar úr `msdy_dualwriteruntimeconfig`-töflunni í Dataverse.

3. Setjið upp [Lausn tvöfaldrar skráningar á aðila og altækri aðsetursbók](https://aka.ms/dual-write-gab) úr AppSource.

4. Í Finance and Operations-forritinu, ef eftirfarandi töflur innihalda gögn, þá skal keyra **Upphaflega samstillingu** fyrir þær.

    + Ávörp
    + Persónubundnar manngerðir
    + Kveðjuorð
    + Titlar tengiliðar
    + Hlutverk ákvarðanatöku
    + Stig viðskiptavildar

5. Í forriti viðskiptavinar skal slökkva á eftirfarandi viðbótarskrefum.

    + Reikningsuppfærsla
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Uppfærsla reiknings
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Uppfærsla reiknings
    + Uppfærsla tengiliðs
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Uppfærsla tengiliðs
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Uppfærsla tengiliðar
    + msdyn_party Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Uppfærsla msdyn_party
    + msdyn_vendor Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Uppfærsla msdyn_vendor

6. Í forriti viðskiptavinar skal slökkva á eftirfarandi verkflæðum:

    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu
    + Uppfæra lánardrottna í reikningstöflu
    + Uppfæra lánardrottna í lánardrottnatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu

7. Í gagnasmiðjunni skal keyra sniðmátið með því að velja **Ræsa núna** eins og sýnt er á eftirfarandi mynd. Þetta ferli gæti tekið nokkrar klukkustundir að ljúka allt eftir því hvert gagnamagnið er.

    ![Setja keyrslu af stað](media/data-factory-trigger.png)

    > [!NOTE]
    > Ef sérstillingar eru fyrir hendi fyrir **Reikning**, **Tengilið** og **Lánardrottin**, þá þarf að breyta sniðmátinu.

8. Flytjið inn nýjar færslur **Aðila** í Finance and Operations-forritinu.

    + Sækið `FONewParty.csv`-skrána úr Azure Blob geymslu. Slóðin er `partybootstrapping/output/FONewParty.csv`.
    + Umbreytið `FONewParty.csv`-skránni í Excel-skrá og flytjið Excel-skrána inn í Finance and Operations-forritið.  Ef csv-innflutningurinn virkar fyrir þig, þá geturðu flutt csv-skrá beint inn. Innflutningurinn gæti tekið nokkrar klukkustundir að keyra, en það fer allt eftir gagnamagninu. Frekari upplýsingar er að finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).

    ![Flytja inn Datavers-aðilafærslur](media/data-factory-import-party.png)

9. Í forritum viðskiptavinar skal kveikja á eftirfarandi viðbótarskrefum:

    + Reikningsuppfærsla
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Uppfærsla reiknings
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Uppfærsla reiknings
    + Uppfærsla tengiliðs
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Uppfærsla tengiliðs
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Uppfærsla tengiliðar
    + msdyn_party Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Uppfærsla msdyn_party
    + msdyn_vendor Update
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Uppfærsla msdyn_vendor

10. Í forritum viðskiptavinar skal virkja eftirfarandi verkflæði ef slökkt var á þeim í fyrri skrefum:

    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu
    + Uppfæra lánardrottna í reikningstöflu
    + Uppfæra lánardrottna í lánardrottnatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu

11. Keyrið varpanir tengdar **Aðilum** eins og lýst er í [Altæk aðila- og aðsetursbók](party-gab.md).

## <a name="troubleshooting"></a>Úrræðaleit

1. Ef ferlið mistekst skal endurkeyra gagnasmiðjuna og byrja á aðgerðinni sem mistókst.
2. Gagnasmiðjan myndar sumar skrár sem hægt er að nota til að staðfesta gögn.
3. Gagnasmiðjan keyrir samkvæmt csv-skránum sem eru afmarkaðar með kommu. Ef reitargildi er með kommu getur það haft áhrif á niðurstöðurnar. Fjarlægja þarf kommurnar.
4. Flipinn **Eftirlit** veitir upplýsingar um öll skref og afgreidd gögn. Veljið tiltekið skref til að kemba þau.

    ![Eftirlitsflipi](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Frekari upplýsingar um sniðmátið

Hægt er að finna athugasemdir um sniðmátið í skránni [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
