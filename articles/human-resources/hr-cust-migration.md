---
title: Dynamics 365 Human Resources flutning viðskiptavina yfir í fjármála- og rekstrarinnviði
description: Þessi grein lýsir flutningi viðskiptavina Microsoft Dynamics 365 Human Resources til fjármála- og rekstrarinnviða.
author: twheeloc
ms.date: 10/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4df9a68ea0128378224bf77bd66423fd2e13fa55
ms.sourcegitcommit: e5b290bac7e8f468167caa1a5607aac6eac9aaea
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2022
ms.locfileid: "9760363"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources flutning viðskiptavina

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Viðskiptavinaflutningur er „lyft-og-færsla“ (hreyfing) á gagnagrunni viðskiptavina yfir í fjármála- og rekstrarinnviði. Sjálfvirk flutningsverkfæri eru notuð fyrir það. Niðurstaðan er nýtt fjármála- og rekstrarumhverfi sem notar mannauðsgagnagrunn viðskiptavinarins.

## <a name="prerequisites"></a>Forkröfur

### <a name="user-access-and-permissions"></a>Notendaaðgangur og heimildir

- The Microsoft Dynamics Lifecycle Services notandi ætti að hafa **Stjórnandi stofnunarinnar** hlutverki.
- Notandinn ætti að geta það [búa til Azure DevOps verkefni](/azure/devops/organizations/projects/create-project) eða nota núverandi Azure DevOps verkefni.
- Notandinn ætti að hafa aðgang að [búa til Azure DevOps Öryggislykill fyrir persónulegan aðgang](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate), eða ætti að hafa tákn sem hægt er að nota.

### <a name="dataverse-environment-backup-sandbox"></a>Dataverse öryggisafrit (Sandbox)

 - Valfrjálst en mælt er með: Endurnýjaðu núverandi sandkassaumhverfi mannauðs með því að nota afrit af framleiðsluumhverfi mannauðs.
 - Búðu til nýtt Dataverse umhverfi með því að nota Power Platform stjórnendamiðstöð.
 - Afritaðu það sem fyrir er Dataverse umhverfi, sem er tengt við sjálfstæða mannauðsappið, við umhverfið sem þú bjóst til í fyrra skrefi.

> [!NOTE]
> Þegar þú bætir við gagnagrunni skaltu ganga úr skugga um að **Virkjaðu Dynamics 365 forrit** valkostur er stilltur á **Já**. Fyrir nákvæmar upplýsingar, sjá [Undirbúa a Power Platform umhverfi](hr-cust-migration.md#prepare-a-power-platform-environment)

### <a name="dataverse-capacity"></a>Dataverse getu

1. Nota **Samantekt** síðu í Power Platform stjórnendamiðstöð til að staðfesta það [Dataverse geymsla](/power-platform/admin/finance-operations-storage-capacity) hefur næga tiltæka afkastagetu fyrir umhverfiseintakið.
2. Ef það er ekki nóg tiltækt afkastagetu skaltu nota [leiðbeiningar til að losa um geymslupláss](/power-platform/admin/free-storage-space) til að draga úr heildarneyslu. Viðskiptavinir geta líka [bæta við viðbótargeymslurými](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Flutningsferli viðskiptavina

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Búðu til verkefni um líftímaþjónustu fyrir mannauðsflutninga

Fyrsta skrefið er að búa til nýtt fjármála- og rekstrarverkefni innleiðingarverkefnis í Lifecycle Services. Viðskiptavinurinn mun hafa fyrirliggjandi Mannauðslífsþjónustuverkefni. Núverandi mannauðsumhverfi verður flutt yfir í nýja fjármála- og rekstrarverkefnið.

Til að búa til nýtt verkefni skaltu fylgja þessum skrefum.

1. Skráðu þig inn á Lifecycle Services sem alþjóðlegur stjórnandi eða tilnefndur notandi þjónustureiknings.
2. Á heimasíðu Lifecycle Services skaltu velja **Búa til/nýja (+)**.
3. Veldu fjármála- og rekstrarforrit sem vöruna.
4. Í **Tilgangur verkefnisins** reit, veldu **Framkvæmd**.
5. Sláðu inn heiti verkefnis og lýsingu.
6. Í **Sérsniðin tegund verkefnis** reit, veldu **Microsoft Dynamics 365 Human Resources fólksflutninga**.
7. Veldu gátreitinn til að samþykkja skilmála og skilyrði.
8. Velja **Stofna**.

Eftir að þú hefur búið til nýtt Lifecycle Services verkefni skaltu fylgja þessum skrefum til að setja það upp og stilla það.

1. Veldu **Inngangur verkefna** til að klára verkefnið um borð. Fyrir frekari upplýsingar, sjá [Inngangur verkefna](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md).

    - Veldu sama svæði og núverandi umhverfi þitt. Þetta val mun ekki hafa áhrif á flutning.
    - Fyrir eldri kerfi, veldu **Annað**.

2. Ljúktu við verkefnisstillingarnar. Sem hluti af þessu skrefi ættir þú að stilla SharePoint Netbókasafn,Azure DevOps, og Azure tengingar ef þeirra er krafist. Fyrir frekari upplýsingar, sjá [Lifecycle Services (LCS) notendahandbók](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Viðskiptavinir geta notað núverandi Azure DevOps verkefni og tilheyrandi öryggistákn fyrir persónulegan aðgang. Ef núverandi verkefni er notað eru stillingarnar sem tengjast verkefninu sjálfkrafa tiltækar og hægt er að skoða þær með tilliti til nákvæmni.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Flyttu mannauðs sandkassaumhverfi

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Búðu þig undir að flytja sandkassaumhverfið

Eftir að nýtt Lifecycle Services verkefni hefur verið búið til og innleiðingarferli verkefnisins hefur verið lokið, ertu tilbúinn til að flytja fyrsta umhverfið þitt. Áður en þú byrjar þetta ferli mælum við með því að þú endurnýjar sandkassaumhverfið sem þú vilt flytja úr framleiðsluumhverfinu þínu á sjálfstæðu innviðina.

#### <a name="prepare-a-power-platform-environment"></a>Undirbúa a Power Platform umhverfi

> [!NOTE]
> Þetta skref á aðeins við um flutning á sandkassaumhverfi. Þegar þú flytur framleiðsluumhverfið, það sem fyrir er Power Platform stjórnendaumhverfi sem er tengt framleiðsluumhverfinu verður flutt áfram. Þegar þú bætir við gagnagrunni skaltu ganga úr skugga um að **Virkjaðu Dynamics 365 forrit** hnappur er stilltur á **Já**. 

- Í stjórnunarmiðstöð Power pallsins, [búa til umhverfi með gagnagrunni](/power-platform/admin/create-environment#create-an-environment-with-a-database) til að nota fyrir sandkassaflutning, eða veldu núverandi umhverfi.
- [Afritaðu umhverfi](/power-platform/admin/copy-environment) að hressa upp á Power Platform umhverfi sem er notað við kortlagningu.

#### <a name="migrate-the-sandbox-environment"></a>Flyttu sandkassaumhverfið

1. Skráðu þig inn á Lifecycle Services sem alþjóðlegur stjórnandi eða tilnefndur notandi þjónustureiknings.

    > [!NOTE]
    > Við mælum með að þú notir nafngreindan notandareikning. Innskráður notandi ætti að hafa **Verkeigandi** eða **Umhverfisstjóri** öryggishlutverk í sjálfstæðu Human Resources Lifecycle Services verkefninu.

2. Opnaðu nýstofnað mannauðsflutningsverkefni.
3. Farðu yfir og ljúktu við viðeigandi stigum flutningsaðferðafræðinnar og innleiðingu verkefnisins.
4. Á stjórnborði verkefnisins, í **Sjálfgefið: Hefðbundið staðfestingarpróf** rúðu, veldu **Flytja HR**.
5. Í **Veldu umhverfi til að flytja** veldu viðeigandi Lifecycle Services verkefni og upprunalega mannauðsumhverfið (frá sjálfstæða mannauðsforritinu þínu).
6. Virkja **Kort til nýtt Power Platform umhverfi**, og veldu viðeigandi Power Platform umhverfi. Veljið síðan **Næst**.
7. Ljúktu við **Dreifingarstillingar (fjármál og rekstur – sandkassi)** töframaður til að staðfesta upplýsingar og afskráningu viðskiptavina, og veldu síðan **Dreifa**.

Umhverfisríkið mun sýna framfarirnar. Ríkinu verður breytt frá **Hleðsla** til **Dreifing** til **Dreifður**.

> [!NOTE]
> Framleiðsluglugginn verður ekki tiltækur fyrr en gátlisti um viðbúnað verkefna er lokið. Fyrir frekari upplýsingar, sjá [Undirbúðu þig fyrir gangsetningu](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="considerations-and-assumptions"></a>Hugleiðingar og forsendur

Mannauðs sandkassaumhverfi er til í Lifecycle Services verkefni á leigjanda sem hefur eftirfarandi eiginleika:

- Sandkassaumhverfi mannauðs er ekki tengt núverandi sameinuðu umhverfi. Aðeins ein flutningur í einu getur verið í gangi fyrir tiltekið mannauðsumhverfi.
- Fjöldi sandkassaumhverfa sem er leyfður í einu byggist á mannauðsleyfi. Ef nóg leyfi hefur verið keypt fyrir leigjandann verða fleiri sandkassaumhverfi skráð í **Umhverfi** glugga verkefnisins.
- Flutningar verða að fara í umhverfi af sömu gerð. Með öðrum orðum, aðeins er hægt að flytja sandkassa í sandkassa eða framleiðslu í framleiðslu.

    > [!NOTE]
    > Aðeins er tekið tillit til mannauðsumhverfistegunda þegar staða framleiðslu eða sandkassa er ákvörðuð. Ef umhverfið er rangt flokkað (þ.e. framleiðsluumhverfi er merkt sem sandkassaumhverfi, eða sandkassaumhverfi er merkt sem framleiðsluumhverfi), hafðu samband við þjónustudeild.

- Ef flutningurinn heppnast ekki munu villuskilaboð birtast og a **Eyða** hnappur verður aðgengilegur. Notaðu þennan hnapp til að eyða misheppnuðum flutningi. Þú getur þá flutt umhverfið aftur.

#### <a name="validate-the-sandbox-migration"></a>Staðfestu sandkassaflutninginn

Eftir að sandkassaflutningsferlinu er lokið skaltu búa til ítarlega prófunaráætlun til að staðfesta og skrá þig af öllum viðskiptaferlum.

Áður en þú byrjar að prófa skaltu staðfesta eftirfarandi upplýsingar:

- Staðfestu að flutt umhverfið sé aðgengilegt á vefslóðinni sem er búin til.
- Staðfestu að notendur hafi aðgang að fluttu sandkassanum.
- Staðfestu að Dataverse umhverfi sem er tengt við flutta sandkassaumhverfið er aðgengilegt.
- Staðfestu mismunandi gögn til að staðfesta að nýjustu gögnin séu tiltæk.
- Ljúktu mikilvægum viðskiptaferlum til staðfestingar.
- Staðfestu að öryggisreglur þínar eigi við.
- Staðfestu að runuvinnslur séu ræstar eins og búist var við.

Þú munt ekki hafa aðgang að fjarstýrðu skrifborði að fluttu sandkassanum. Þú getur notað sjálfsafgreiðslugetu og verkfæri til að framkvæma eftirfarandi aðgerðir fyrir Tier 2+ sandkassaumhverfið þitt:

- Aðgangur að [Azure SQL gagnagrunnur](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database).
- Aðgangur [log skrár](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files).
- Notaðu [perfmon verkfæri](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools).
- Snúa [Kveikt/slökkt á viðhaldsstillingu](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs).
- Endurræsa [þjónusta](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services).
- Stilltu [Aðhvarfssvíta sjálfvirkniverkfæri](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool).

Fyrir frekari upplýsingar, sjá [Algengar spurningar um sjálfsafgreiðslu](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Flyttu framleiðsluumhverfi mannauðs

Eftir að þú hefur lokið við að flytja og staðfesta sandkassaumhverfi skaltu fylgja þessum skrefum til að flytja framleiðsluumhverfið.

#### <a name="prerequisites"></a>Forkröfur

- Áskriftarmatið ætti að vera lokið.
- The Go-live [viðbúnaðarmat](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) ætti að vera lokið.

#### <a name="migrate-the-production-environment"></a>Flyttu framleiðsluumhverfið

1. Skráðu þig inn á Lifecycle Services sem alþjóðlegur stjórnandi eða tilnefndur notandi þjónustureiknings.

    > [!NOTE]
    > Við mælum með að þú notir nafngreindan notandareikning. Innskráður notandi ætti að hafa **Verkeigandi** eða **Umhverfisstjóri** öryggishlutverk í Lifecycle Services verkefninu.

2. Opnaðu nýja mannauðsflutningaverkefnið.
3. Farðu yfir og ljúktu við viðeigandi stigum flutningsaðferðafræðinnar og innleiðingu verkefna.
4. Á stjórnborði verkefnisins, í **Framleiðsla** rúðu, veldu **Flytja HR**.
5. Í **Veldu umhverfi til að flytja** veldu viðeigandi Lifecycle Services verkefni og upprunalega mannauðsumhverfið (frá sjálfstæða mannauðsforritinu þínu). Veljið síðan **Næst**.
6. Ljúktu við **Dreifingarstillingar (fjármál og rekstur – sandkassi)** töframaður til að staðfesta upplýsingar og afskráningu viðskiptavina, og veldu síðan **Dreifa**.

Umhverfisríkið mun sýna framvindu dreifingarinnar. Ríkinu verður breytt frá **Hleðsla** til **Dreifing** til **Dreifður**.

#### <a name="post-migration-considerations"></a>Athugasemdir eftir búferlaflutninga

- Notaðu það nýjasta [gæðauppfærslur](/fin-ops-core/fin-ops/get-started/quality-updates) við umhverfi þitt.
- Ef þú ert að nota [sýndarborðum](hr-admin-integration-common-data-service-virtual-entities.md), endurstilla endapunktana.
- Endurstilla samþættingu tvískrifa. Metið hvaða einingar verða að vera virkjaðar.
- Íhugaðu að nota sýndartöflur til að skipta um tvískrift fyrir samþættingu.

#### <a name="dual-write-integration"></a>Tvöföld skrif – samþætting

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Settu upp Microsoft Power Platform tvískrifa samþætting

1. Farðu í Power Platform stjórnendamiðstöð og veldu **Umhverfi** í vinstri flakk.
2. Veldu áður afritað/uppfært umhverfi og staðfestu að ástandið sé það **Tilbúið**.
3. Farðu í Lifecycle Services og staðfestu að staða flutningsverkefnisins sé **Dreifður**.
4. Undir fluttu umhverfið velurðu **Allar upplýsingar** til að fara yfir frekari upplýsingar og [setja upp tvískrifa forrit](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. Í **Tvöfalt skrifa forritsstillingar** veldu gátreitinn til að samþykkja að kortleggja og samstilla gögn á milli gagnagrunna og veldu síðan **Stilla**.
6. Þegar skilaboðakassi lætur þig vita um vel heppnaða uppsetningu með tvöföldum skrifum skaltu velja **Allt í lagi**.
7. Þú getur fylgst með framvindu stillingar í smáatriðum.
8. Þegar uppsetningu er lokið skaltu velja **Tengill á Power Platform umhverfi** til að samstilla fyrirliggjandi gagnaeiningar.
9. Þegar staðan gefur til kynna að búið sé að tengja umhverfið með góðum árangri skaltu fara í Power Platform stjórnendamiðstöð til að skoða og velja viðeigandi gagnaeiningar.
10. Í vinstri glugganum velurðu **Dynamics 365 forrit \> Auðlindir**.
11. Staðfestu að staða mannauðsappsins með tvöföldum skrifum sé **Virkt**.
12. Veldu tvískrifað mannauðsforritið og veldu síðan **Settu upp**.
13. Í **Settu upp tvískrifa Dynamics 365 Human Resources app** veldu viðeigandi umhverfi til að setja upp pakkann í.
14. Veldu gátreitinn til að samþykkja þjónustuskilmálana og veldu síðan **Settu upp**.
15. Í Dynamics 365 app umhverfinu verður staðan **Er að setja upp** meðan uppsetning er í gangi. Það verður uppfært til **Uppsett** þegar uppsetningu er lokið.

##### <a name="review-and-apply-a-dual-write-solution"></a>Skoðaðu og notaðu tvískrifalausn

1. Í nýju fjármála- og rekstrarumhverfi, farðu til **Gagnastjórnun \> Tvöfalt skrifa**.
2. Veldu **Notaðu lausn**.
3. Í glugganum velurðu **Dynamics uppsettar lausnir**, **-write forrit kjarnaeiningakort**, og **Dynamics 365 Human Resources kortum**. Veldu síðan **Sækja um**. Skilaboð staðfesta að verið sé að beita lausninni. Eftir að lausnin hefur verið beitt með góðum árangri verða öll tiltæk töflukort sýnd.
4. Skoðaðu tiltæk töflukort til að velja og keyra samþættinguna með því að nota tvískrift.
5. Þegar þú keyrir tvískrifa samþættingu í fyrsta skipti fyrir töflukort skaltu velja **Upphafleg samstilling** gátreit. Ef það er fyrirliggjandi samþætting frá uppruna mannauðsumhverfinu þarftu ekki að velja **Upphafleg samstilling** gátreitinn þegar þú keyrir samþættingu fyrir töflukort.

#### <a name="recommended-practices"></a>Ráðlagðar aðferðir

Þessi hluti lýsir ráðleggingum um flutning frá sjálfstæðum innviðum yfir í fjármála- og rekstrarinnviði.

- Við mælum eindregið með því að þú vinnur með þínum Microsoft Dynamics samstarfsaðila til að fá aðstoð við flutning mannauðsumhverfis þíns.
- Skipuleggðu viðeigandi tíma til að gera fulla notendasamþykkisprófun (UAT) á sandkassaflutta umhverfinu.
- Skipuleggðu og skjalfestu ítarleg skref til að flytja samþættingar yfir í flutta umhverfið.
- Búðu til ítarlegan gátlista til að útlista niðurskurðarferlið fyrir flutninginn þinn.
- Skipuleggðu viðeigandi magn af niður í miðbæ fyrir fyrirtæki þitt á meðan þú gerir flutninginn.
- Við mælum eindregið með því að FastTrack-hæfir viðskiptavinir vinni með FastTrack lausnararkitektinum sínum til að fá aðstoð við að hafa umsjón með flutningsferlinu.
- Við mælum eindregið með því að þú endurnýjar sandkassaumhverfið þitt í sjálfstæðum innviðum áður en þú gerir fyrstu flutninginn. Þessi endurnýjun ætti að innihalda þitt Dataverse umhverfi sem er tengt við sandkassaumhverfið sem þú ætlar að flytja til.
- Við mælum eindregið með því að þú notir þjónustureikning þegar þú dreifir, flytur og býrð til Lifecycle Services verkefnið þitt.
- Ætlaðu að uppfæra sandkassaumhverfið fyrir UAT löggildingu á nýjustu útgáfunni fyrir almenna tiltæka (GA). Fyrir frekari upplýsingar, sjá [sjónarmiðum](hr-infrastructure-merge.md#considerations).
